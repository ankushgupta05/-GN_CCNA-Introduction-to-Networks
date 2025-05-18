Here’s a **summary and explanation** of the content from sections **11.7.1 and 11.7.2** on subnetting with **Private vs Public IPv4 address space** and how to **minimize unused hosts while maximizing subnets**:

---

## 🔐 **11.7.1: Subnet - Private vs Public IPv4 Address Space**

### 🌐 **Enterprise Network Structure**

* **Intranet**:

  * Internal part of the company.
  * Uses **private IPv4 addresses** (e.g., `10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`).
  * Not directly accessible from the Internet.

* **DMZ (Demilitarized Zone)**:

  * Holds services accessible from the Internet (e.g., web/mail servers).
  * Uses **public IPv4 addresses**.
  * Sits between the internal network and the Internet.

### 🧩 **Subnetting in Intranet (Private IPs)**

* Flexible due to large address spaces.
* **Example: `10.0.0.0/8`**

  * Subnetting with `/16`:

    * Yields **256 subnets**, each with **65,534 hosts**.
  * Subnetting with `/24`:

    * Yields **65,536 subnets**, each with **254 hosts**.
* Can use a variety of masks (`/12`, `/18`, `/20`, etc.) to suit organizational needs.

> ✅ Using private addresses offers **flexibility** in subnet design without concerns of public IP exhaustion.

### 🌍 **Subnetting in DMZ (Public IPs)**

* Must be **public IPs** (accessible from outside).
* Due to **IPv4 exhaustion**, public addresses are **limited**.
* Efficient use is **critical**.
* Uses **VLSM (Variable Length Subnet Masking)**:

  * Allows subnetting using **different subnet masks**.
  * Helps **minimize unused host IPs** in each subnet.

---

## 🧮 **11.7.2: Minimize Unused Hosts & Maximize Subnets**

### 📉 **Inverse Relationship: Subnets vs Hosts**

* Subnetting means borrowing bits from the host portion:

  * More **subnets** → **fewer hosts per subnet**
  * More **hosts per subnet** → **fewer subnets**

### 🧠 **Key Formula**:

* Usable host addresses per subnet = `2^n - 2`

  * Where `n` = number of host bits
  * Subtract 2 for:

    * Network address (all 0s)
    * Broadcast address (all 1s)

### 🎯 **Planning Considerations**:

* Consider:

  1. **Maximum number of hosts** needed on the largest subnet.
  2. **Total number of subnets** required.
* Leave room for:

  * **Future expansion** in hosts per subnet.
  * **More subnets** in case of organizational growth.

---

### 📌 **In Summary**:

| **Component**    | **Address Type** | **Subnet Strategy**                 | **Goal**                            |
| ---------------- | ---------------- | ----------------------------------- | ----------------------------------- |
| Intranet         | Private IPv4     | Flexible masks (`/16`, `/24`, etc.) | Ease of subnetting, scalability     |
| DMZ              | Public IPv4      | VLSM (custom subnet masks)          | Efficient use of limited public IPs |
| General Strategy | Any              | Based on host/subnet need           | Balance between subnets and hosts   |

Let me know if you want the subnetting tables for /16 or /24 or a visual topology diagram explained too.
Here's a clear and organized summary of **Example 11.7.3 – Efficient IPv4 Subnetting**:

---

### 🔶 **Objective**

Efficiently subnet the private network `172.16.0.0/22` to support:

* **5 sites** (1 corporate HQ + 4 branch offices)
* **10 subnets** required (each site + ISP links)
* **Largest subnet needs 40 hosts**

---

### 📌 **Network Overview**

* **Given network**: `172.16.0.0/22`
* **Total Host Bits**: 10 → `2^10 - 2 = 1022 hosts`
* **Private IP space**: Used instead of public IP

---

### 📊 **Subnetting Strategy**

#### ➤ **Why Subnet?**

* 5 sites → 5 routers → 5 ISP connections
* 5 subnets for site LANs + 5 subnets for router-ISP links = **10 subnets**

#### ➤ **Largest Host Requirement**:

* Corporate HQ: **40 hosts**
* Needs **6 host bits** → `2^6 - 2 = 62 hosts`
* Therefore, **keep 6 host bits**, borrow the remaining **4 bits** from the 10 host bits

#### ➤ **Borrowing 4 bits**:

* `10 host bits - 4 = 6 host bits`
* New prefix: **/26**
* Subnet mask: **255.255.255.192**
* Number of subnets: `2^4 = 16 subnets`
* Hosts per subnet: `2^6 - 2 = 62`

---

### 🗂️ **Subnet Details (/26)**

| Subnet # | Subnet Address  | Range Start  | Range End    | Broadcast Address |
| -------- | --------------- | ------------ | ------------ | ----------------- |
| 0        | 172.16.0.0/26   | 172.16.0.1   | 172.16.0.62  | 172.16.0.63       |
| 1        | 172.16.0.64/26  | 172.16.0.65  | 172.16.0.126 | 172.16.0.127      |
| 2        | 172.16.0.128/26 | 172.16.0.129 | 172.16.0.190 | 172.16.0.191      |
| 3        | 172.16.0.192/26 | 172.16.0.193 | 172.16.0.254 | 172.16.0.255      |
| 4        | 172.16.1.0/26   | 172.16.1.1   | 172.16.1.62  | 172.16.1.63       |
| 5        | 172.16.1.64/26  | 172.16.1.65  | 172.16.1.126 | 172.16.1.127      |
| 6        | 172.16.1.128/26 | 172.16.1.129 | 172.16.1.190 | 172.16.1.191      |
| 7        | 172.16.1.192/26 | 172.16.1.193 | 172.16.1.254 | 172.16.1.255      |
| 8        | 172.16.2.0/26   | 172.16.2.1   | 172.16.2.62  | 172.16.2.63       |
| 9        | 172.16.2.64/26  | 172.16.2.65  | 172.16.2.126 | 172.16.2.127      |

---

### 🧭 **Subnet Assignments**

| Site / Link        | Subnet Assigned | Hosts Needed   |
| ------------------ | --------------- | -------------- |
| Corporate HQ (LAN) | 172.16.0.64/26  | 40             |
| Corp. HQ ↔ ISP     | 172.16.0.0/26   | Point-to-point |
| Branch 1 (LAN)     | 172.16.0.192/26 | 25             |
| Branch 1 ↔ ISP     | 172.16.0.128/26 | P2P            |
| Branch 2 (LAN)     | 172.16.1.64/26  | 30             |
| Branch 2 ↔ ISP     | 172.16.1.0/26   | P2P            |
| Branch 3 (LAN)     | 172.16.1.192/26 | 10             |
| Branch 3 ↔ ISP     | 172.16.1.128/26 | P2P            |
| Branch 4 (LAN)     | 172.16.2.64/26  | 15             |
| Branch 4 ↔ ISP     | 172.16.2.0/26   | P2P            |

---

### ✅ **Conclusion**

* Borrowing 4 bits created **16 /26 subnets**
* **10 subnets** used to meet current needs (5 sites + 5 ISP links)
* **6 subnets remain available** for future growth

---
Here is the completed table for the activity **"Determine the Number of Bits to Borrow"** based on the number of required hosts:

| Hosts Needed | Subnet Mask (binary)                | Subnet Mask (decimal) | Prefix Notation (/x) |
| ------------ | ----------------------------------- | --------------------- | -------------------- |
| 250          | 11111111.11111111.11111111.00000000 | 255.255.255.0         | /24                  |
| 25           | 11111111.11111111.11111111.11100000 | 255.255.255.224       | /27                  |
| 1000         | 11111111.11111111.11111100.00000000 | 255.255.252.0         | /22                  |
| 75           | 11111111.11111111.11111111.10000000 | 255.255.255.128       | /25                  |
| 10           | 11111111.11111111.11111111.11110000 | 255.255.255.240       | /28                  |
| 500          | 11111111.11111111.11111110.00000000 | 255.255.254.0         | /23                  |

### 📌 Explanation:

To determine the required subnet mask:

* Use the formula: `2^n - 2 ≥ number of hosts`
* Then subtract `n` from 32 to get the prefix length.
* Convert the prefix to binary and decimal form for the subnet mask.

Let me know if you want a breakdown of any specific row.
