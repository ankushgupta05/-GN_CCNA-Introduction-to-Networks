You're studying a key concept in networking: **Variable Length Subnet Masking (VLSM)**, which helps efficiently allocate IP addresses based on actual host requirements—unlike traditional fixed-size subnetting that can waste many addresses.

Let’s break down and summarize the main concepts from **sections 11.8.1 to 11.8.3** in a clear, digestible format.

---

### 🔍 **Key Concepts Explained**

#### 🔹 Traditional Subnetting (Fixed Length)

* Every subnet has the same number of host addresses.
* Example: Subnetting `192.168.20.0/24` into `/27` creates **8 subnets**, each with **30 usable host addresses** (`2^5 - 2 = 30`).
* Works well **only** if all subnets have similar host needs.

#### 🔹 The Problem

* You may have:

  * LANs that need 25, 20, 15, and 28 hosts.
  * Router-to-router WAN links that need only **2 hosts each**.
* Using `/27` for all wastes IP addresses:

  * WAN links use 2 IPs but get 30 per subnet → **28 wasted × 3 WANs = 84 wasted IPs**.
* This inefficiency also limits future growth (fewer subnets available).

---

### ✅ **What is VLSM (Variable Length Subnet Masking)?**

* VLSM **lets you use different subnet masks** depending on how many hosts are needed in each subnet.
* You **subnet a subnet** by assigning:

  * **Smaller subnets** (e.g., `/30` with 2 usable IPs) for WAN links.
  * **Larger subnets** (e.g., `/27`, `/26`) for LANs based on host requirements.

---

### 🧠 **Advantages of VLSM**

| Feature                       | Benefit                             |
| ----------------------------- | ----------------------------------- |
| Custom subnet sizes           | Match IP space to host requirements |
| Reduces waste                 | Saves unused addresses              |
| Maximizes address usage       | Leaves room for growth              |
| Efficient for public IPv4 use | Conserves limited IP space          |

---

### 🏗️ Example Recap from Scenario

| Subnet Purpose     | Hosts Needed | Traditional (/27) | VLSM Alternative |
| ------------------ | ------------ | ----------------- | ---------------- |
| LAN A (R1)         | 25           | /27 (OK)          | /27 (Same)       |
| LAN B (R2)         | 20           | /27 (OK)          | /27 or /28       |
| LAN C (R3)         | 15           | /27 (Wasted)      | /28              |
| LAN D (R4)         | 28           | /27 (Just fits)   | /27 or /26       |
| WANs (R1-R2, etc.) | 2 each       | /27 (Wasted)      | /30              |

---

### 🧮 **VLSM Address Planning Tips**

1. **Sort subnets by host requirements (largest to smallest).**
2. **Allocate larger subnets first** to avoid overlaps.
3. Use **/30** for point-to-point links.
4. Reuse remaining address space for smaller subnets.

---

### 🧾 Summary

* Traditional subnetting = same size blocks → inefficient for mixed needs.
* VLSM = flexible, efficient, conserves IP addresses.
* In IPv4, VLSM is essential due to the limited address space.
* IPv6 has so much space that VLSM is less critical.

---

### Summary: **11.8.4 VLSM (Variable Length Subnet Masking)**

---

#### ✅ **Traditional Subnetting vs. VLSM**

| Aspect                 | Traditional Subnetting                                | VLSM                                                                    |
| ---------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------- |
| **Subnet Size**        | All subnets are equal in size                         | Subnets can be of different sizes                                       |
| **Subnet Mask**        | Same across all subnets                               | Varies per subnet                                                       |
| **Address Efficiency** | Leads to wasted addresses when fewer hosts are needed | Efficient use of address space by fitting subnets to actual size needed |
| **Use Case**           | Simpler, rigid networks                               | Complex topologies with varied subnet requirements                      |

---

#### 📌 **VLSM Key Concept**

* **"Subnetting a subnet"**: You can take an existing subnet and divide it further by borrowing more bits.
* This enables **more granular control** over IP address allocation.

---

#### 💡 **Why /30 for Router-to-Router Links?**

* Only **2 usable IP addresses** are needed (one for each router interface).
* Using a **/30 subnet mask** (i.e., `255.255.255.252`) leaves:

  * 2 bits for host = `2² - 2 = 2` usable addresses

---

#### 📊 **Example Network – 192.168.20.0/24**

| Subnet                | Address            | CIDR | Purpose             | Hosts    |
| --------------------- | ------------------ | ---- | ------------------- | -------- |
| Subnet 0              | 192.168.20.0       | /27  | Building A (R1 LAN) | 25 hosts |
| Subnet 1              | 192.168.20.32      | /27  | Building B (R2 LAN) | 20 hosts |
| Subnet 2              | 192.168.20.64      | /27  | Building C (R3 LAN) | 15 hosts |
| Subnet 3              | 192.168.20.96      | /27  | Building D (R4 LAN) | 28 hosts |
| Subnet 7:0            | 192.168.20.224     | /30  | R1 ↔ R2 link        | 2 hosts  |
| Subnet 7:1            | 192.168.20.228     | /30  | R2 ↔ R3 link        | 2 hosts  |
| Subnet 7:2            | 192.168.20.232     | /30  | R3 ↔ R4 link        | 2 hosts  |
| Remaining /30 subnets | 192.168.20.236–252 | /30  | Unused              | -        |

---

#### 🔢 **Binary Subnetting Breakdown**

| Field              | Binary Portion                                      |
| ------------------ | --------------------------------------------------- |
| Network (/24)      | `11000000.10101000.00010100`                        |
| 1st Subnet (/27)   | + `000` (3 bits borrowed)                           |
| Further VLSM (/30) | + `000` + `000` (3 more bits) → total 6 subnet bits |

This means the original `/24` network has:

* **4 LAN subnets (/27)**: 30 usable hosts each
* **1 of those subnets (/27)** split into **8 /30 subnets** for WANs

---

#### 📘 **Conclusion**

VLSM allows you to:

* Use your IP space efficiently.
* Assign **larger subnets to LANs** with more hosts.
* Assign **tiny subnets (/30)** for point-to-point WAN links.
* Avoid waste and **optimize IPv4 usage**, especially important with limited IPs.

Let's walk through **VLSM subnetting** for the network `192.168.5.0/24` to support **50 users per subnet**.

---

### 🔹 Step-by-Step Breakdown:

#### ✅ Step 1: Determine subnet mask needed for 50 users

* You need at least **50 usable IPs** per subnet.
* Formula: `2^n - 2 ≥ 50`

  * `2^6 = 64`, so `64 - 2 = 62 usable addresses`
* That means a **/26** subnet is sufficient (because /26 = 255.255.255.192 = 64 IPs, 62 usable).

---

### ✅ **Table 1 - First Subnets Calculation (Fixed Size /26)**

| Subnet # | IP Range                      | Prefix Notation | Subnet Mask     |
| -------- | ----------------------------- | --------------- | --------------- |
| 1        | 192.168.5.0 - 192.168.5.63    | /26             | 255.255.255.192 |
| 2        | 192.168.5.64 - 192.168.5.127  | /26             | 255.255.255.192 |
| 3        | 192.168.5.128 - 192.168.5.191 | /26             | 255.255.255.192 |
| 4        | 192.168.5.192 - 192.168.5.255 | /26             | 255.255.255.192 |

---

### 🔘 Based on your activity instructions, here’s what to **click/select**:

1. **Click the new subnet mask (decimal):**
   ✅ **255.255.255.192**

2. **Click the first prefix notation:**
   ✅ **/26**

3. **Click the first full subnet range:**
   ✅ **192.168.5.0 - 192.168.5.63**

4. **Click the second full subnet range:**
   ✅ **192.168.5.64 - 192.168.5.127**

5. **Click the last full subnet range:**
   ✅ **192.168.5.192 - 192.168.5.255**

---
Let's break this down clearly for **Table 2 - VLSM Calculation** using `192.168.5.0/24`, where the network is being **subnetted with Variable Length Subnet Masks (VLSM)**.

From **Table 1**, the **second /26 subnet** was:

🔹 `192.168.5.64 - 192.168.5.127` → this full block is now being **split further using VLSM**.

---

### 🔹 Step-by-Step: Splitting 192.168.5.64/26 into smaller VLSM subnets

#### 🧮 VLSM: New subnet mask

We are breaking `/26` into smaller subnets (e.g., `/27`, `/28`).

* `/27` → 32 IPs (30 usable)

  * First: `192.168.5.64 - 192.168.5.95`
  * Second: `192.168.5.96 - 192.168.5.127`

---

### ✅ What you should click/select:

1. **Click the second full subnet range (/26) from Table 1**
   ✅ **192.168.5.64 - 192.168.5.127**

2. **Click the new VLSM subnet mask (decimal)**
   ✅ **255.255.255.224**
   (*This is the decimal for /27*)

3. **Click the VLSM prefix notation**
   ✅ **/27**

4. **Click the first full VLSM subnet range**
   ✅ **192.168.5.64 - 192.168.5.95**

5. **Click the last full VLSM subnet range**
   ✅ **192.168.5.96 - 192.168.5.127**

---

Let me know if you need help visualizing a diagram for this or calculating even smaller subnets like /28 or /29.
