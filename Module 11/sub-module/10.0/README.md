Here is a detailed explanation of each question from **11.10.4 Module Quiz - IPv4 Addressing**, including:

* ✅ **Correct answer**
* ❌ **Why other options are incorrect**
* 📘 **Explanation**

---

### **Question 1**

**What is the prefix length notation for the subnet mask 255.255.255.224?**
✅ **Answer:** `/27`

📘 **Explanation:**

* 255.255.255.224 → binary: `11111111.11111111.11111111.11100000` → 27 ones → `/27`

**Options Breakdown:**

* ❌ `/25` → 255.255.255.128
* ❌ `/26` → 255.255.255.192
* ✅ `/27` → ✔️ Correct
* ❌ `/28` → 255.255.255.240

---

### **Question 2**

**How many valid host addresses are available on a subnet with /26 mask?**
✅ **Answer:** `62`

📘 **Explanation:**

* /26 = 32 - 26 = 6 bits for host
* $2^6 = 64$ total addresses
* Valid host addresses = 64 - 2 = **62**

**Options Breakdown:**

* ❌ `254` → /24
* ❌ `190` → /25 (wrong math)
* ❌ `192` → total, not valid
* ✅ `62` → ✔️ Correct
* ❌ `64` → includes network & broadcast

---

### **Question 3**

**Which subnet mask would be used if 5 host bits are available?**
✅ **Answer:** `255.255.255.224`

📘 **Explanation:**

* 5 bits → $2^5 = 32$ total → 30 usable
* 32-bit IP - 5 = 27 bits → `/27` → 255.255.255.224

**Options Breakdown:**

* ❌ `255.255.255.0` → /24 → 8 host bits
* ❌ `255.255.255.128` → /25 → 7 host bits
* ✅ `255.255.255.224` → ✔️ 5 host bits
* ❌ `255.255.255.240` → /28 → 4 host bits

---

### **Question 4**

**Subnetting 192.168.10.0/24 into /26 — how many subnets?**
✅ **Answer:** `4`

📘 **Explanation:**

* /24 to /26 → 2 extra bits for subnetting
* $2^2 = 4$ subnets

**Options Breakdown:**

* ❌ `1` → no subnetting
* ❌ `2` → 1 extra bit only
* ✅ `4` → ✔️ 2 bits = 4 subnets
* ❌ `8`, `16`, `64` → incorrect calculation

---

### **Question 5**

**Subnet mask for /20?**
✅ **Answer:** `255.255.240.0`

📘 **Explanation:**

* /20 = 8+8+4 = `255.255.240.0`

**Options Breakdown:**

* ❌ `255.255.255.248` → /29
* ❌ `255.255.224.0` → /19
* ✅ `255.255.240.0` → ✔️
* ❌ `255.255.255.0` → /24
* ❌ `255.255.255.192` → /26

---

### **Question 6**

**Which statement is true about VLSM?**
✅ **Answer:** `The size of each subnet may be different, depending on requirements.`

📘 **Explanation:**

* VLSM = Variable-Length Subnet Masking → subnets of different sizes

**Options Breakdown:**

* ❌ `Each subnet is the same size` → FLSM, not VLSM
* ✅ `...different...` → ✔️ Correct
* ❌ `...only be subnetted once` → False
* ❌ `...bits are returned...` → False

---

### **Question 7**

**Why does Layer 3 device perform ANDing on IP and mask?**
✅ **Answer:** `To identify the network address of the destination network`

📘 **Explanation:**

* ANDing reveals the **network portion** of IP address.

**Options Breakdown:**

* ❌ `Broadcast address` → Calculated differently
* ❌ `Host address` → Host = leftover bits
* ❌ `Faulty frames` → Layer 2 issue
* ✅ `Network address` → ✔️ Correct

---

### **Question 8**

**Usable IPs on 192.168.1.0/27?**
✅ **Answer:** `30`

📘 **Explanation:**

* /27 → 5 host bits → $2^5 = 32$ → 32 - 2 = **30**

**Options Breakdown:**

* ❌ `256` → /24
* ❌ `254` → /24 usable
* ❌ `62` → /26
* ✅ `30` → ✔️ Correct
* ❌ `16`, `32` → total or incorrect

---

### **Question 9**

**Subnet mask with exactly 4 host bits?**
✅ **Answer:** `255.255.255.240`

📘 **Explanation:**

* 4 bits → 32 - 4 = 28 → /28 → `255.255.255.240`

**Options Breakdown:**

* ❌ `255.255.255.224` → /27 → 5 bits
* ❌ `255.255.255.128` → /25 → 7 bits
* ✅ `255.255.255.240` → ✔️ Correct
* ❌ `255.255.255.248` → /29 → 3 bits

---

### **Question 10**

**Which two are parts of an IPv4 address? (Choose two)**
✅ **Answers:**

* `Network portion`
* `Host portion`

📘 **Explanation:**

* IP = Network + Host
* Subnet mask separates them

**Options Breakdown:**

* ✅ `Network portion` → ✔️
* ✅ `Host portion` → ✔️
* ❌ `Subnet portion` → not a direct part
* ❌ `Logical portion` → vague
* ❌ `Physical portion` → MAC, not IP
* ❌ `Broadcast portion` → not part of address

---

### **Question 11**

**/26 network — how many usable host IPs?**
✅ **Answer:** `62`

📘 **Explanation:**

* /26 = 6 bits → 64 total → 64 - 2 = **62**

**Options Breakdown:**

* ❌ `64` → total, not usable
* ❌ `30` → /27
* ✅ `62` → ✔️ Correct
* ❌ `32`, `16`, `14` → smaller subnets

---

### **Question 12**

**172.17.4.250/24 represents...?**
✅ **Answer:** `Host address`

📘 **Explanation:**

* Not network (.0) or broadcast (.255)
* Therefore, it’s a host address

**Options Breakdown:**

* ❌ `Network address` → 172.17.4.0
* ❌ `Multicast` → 224.0.0.0+
* ✅ `Host address` → ✔️
* ❌ `Broadcast address` → 172.17.4.255

---

### **Question 13**

**/28 subnet — how many usable IPs?**
✅ **Answer:** `14`

📘 **Explanation:**

* /28 = 4 bits → $2^4 = 16$ → 16 - 2 = **14 usable**

**Options Breakdown:**

* ❌ `256`, `254` → /24
* ❌ `62` → /26
* ❌ `32`, `16` → total or too big
* ✅ `14` → ✔️ Correct

---

### **Question 14**

**Purpose of subnet mask with IP?**
✅ **Answer:** `To determine the subnet to which the host belongs`

📘 **Explanation:**

* Mask shows which part is network vs. host

**Options Breakdown:**

* ❌ `Uniquely identify...` → IP does that
* ❌ `Public/private` → Prefix range, not mask
* ✅ `Determine subnet` → ✔️
* ❌ `Mask to outsiders` → Not the purpose

---

### **Question 15**

**Smallest subnet has mask 255.255.255.224 — usable addresses?**
✅ **Answer:** `30`

📘 **Explanation:**

* 255.255.255.224 → /27 → 5 bits → 32 - 2 = **30 usable**

**Options Breakdown:**

* ❌ `2`, `6`, `14` → smaller subnets
* ✅ `30` → ✔️ Correct
* ❌ `62` → /26

---

Let me know if you'd like this in table format (Markdown/README) or exported as a file.
