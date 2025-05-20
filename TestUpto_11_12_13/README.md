Here’s a full breakdown of **Questions 1 to 15** with selected answers, explanations on **why** the selected option is correct, and why the others are not.

---

### ✅ **Question 1**

**Match the network with the correct IP address and prefix that will satisfy the usable host addressing requirements.**

We assume the following host requirements (based on subnet sizes):

* **/25** → 126 usable hosts
* **/26** → 62 usable hosts
* **/27** → 30 usable hosts
* **/30** → 2 usable hosts

**Correct Matching:**

* **Network A** → `192.168.0.128 /25` → Large network (126 hosts)
* **Network B** → `192.168.0.0 /26` → Medium network (62 hosts)
* **Network C** → `192.168.0.96 /27` → Small network (30 hosts)
* **Network D** → `192.168.0.80 /30` → Point-to-point (2 hosts)

---

### ✅ **Question 2**

**Usable number of host IPs on /26?**

* **/26** = 64 total addresses
* Usable = 64 - 2 (network + broadcast) = **62**

✅ Correct: **62**

🟥 Incorrect options:

* **64** → includes unusable addresses
* **256, 254** → /24
* **32, 16** → /27, /28 respectively

---

### ✅ **Question 3**

**Second usable subnet of 192.168.1.0/24 when divided into 4 equal subnets.**

* /24 → 256 total IPs
* Divide into 4 → **/26** subnets (64 IPs each)

Subnets:

1. 192.168.1.0/26
2. **192.168.1.64/26** ← ✅ second usable
3. 192.168.1.128/26
4. 192.168.1.192/26

✅ Correct: **192.168.1.64 /26**

🟥 Incorrect:

* 192.168.1.32 → /27 size (not /26)
* 192.168.1.8, 192.168.1.64/240 → incorrect ranges

---

### ✅ **Question 4**

**Host addresses in 172.16.128.0 with mask 255.255.252.0 (/22)**

* /22 = 1024 total IPs
* Usable = 1024 - 2 = **1022**

✅ Correct: **1022**

🟥 Incorrect:

* 1024 → includes reserved IPs
* 2046, 2048 → /21
* 512, 510 → /23

---

### ✅ **Question 5**

**IPv4 Multicast Address Range:**
✅ Correct: **224.0.0.0 – 239.255.255.255**

🟥 Incorrect:

* 240+ → reserved for future
* 169.254+ → link-local
* 127.0+ → loopback

---

### ✅ **Question 6**

**Need 10 and 18 hosts → min /28 (16 IPs), /27 (32 IPs)**

* 192.168.1.64/27 → 32 IPs (for 18-host network) ✅
* 192.168.1.96/28 → 16 IPs (for 10-host network) ✅

✅ Correct:

* **192.168.1.64/27**
* **192.168.1.96/28**

🟥 Incorrect:

* 192.168.1.16 → wrong base
* 192.168.1.128 → outside original range
* 192.168.1.192 → overlaps with wrong block

---

### ✅ **Question 7**

**Broadcast for 172.16.16.0/22**

* /22 → block size = 4 subnets = 172.16.16.0 – 172.16.19.255
* Last address = **172.16.19.255** ✅

🟥 Incorrect:

* 172.16.23.255 → /21
* 172.16.16.255 → end of /24
* 172.16.255.255 → entire class B range
* 172.16.20.255 → outside range

---

### ✅ **Question 8**

**Usable addresses in 192.168.10.128/26**

* /26 = 64 total
* Usable = 62 ✅

✅ Correct: **62**

🟥 Incorrect:

* 64 → includes network/broadcast
* 30 → /27
* 32 → /27

---

### ✅ **Question 9**

**Bits to borrow for 5 subnets?**

* Need **5 subnets** → minimum **3 bits** (2³ = 8 ≥ 5) ✅

✅ Correct: **Three**

🟥 Incorrect:

* Two → only 4 subnets
* Four → 16 subnets (overkill)
* Five → 32 subnets

---

### ✅ **Question 10**

**Why does 192.168.25.10 not work over the internet?**

* It's a **Private IP** (192.168.0.0/16)

✅ Correct: **This is a private IP address**

🟥 Incorrect:

* Not link-local
* Not loopback
* No address conflict mentioned

---

### ✅ **Question 11**

**Subnet mask for 126 hosts?**

* 2⁷ = 128 → 126 usable
* **/25 = 255.255.255.128** ✅

✅ Correct: **255.255.255.128**

🟥 Incorrect:

* /24 = 254 hosts (okay but not optimal)
* /27 = 30 hosts
* /28 = 14 hosts

---

### ✅ **Question 12**

**Protocol supporting SLAAC (Stateless Address Autoconfiguration)**

✅ Correct: **ICMPv6**

🟥 Incorrect:

* DHCPv6 → Stateful
* UDP → Transport layer
* ARPv6 → Doesn’t exist

---

### ✅ **Question 13**

**Prefix of 2001\:DB8\:BC15\:A:12AB::1/64**

* First 64 bits: `2001:DB8:BC15:A`

✅ Correct: **2001\:DB8\:BC15\:A**

🟥 Incorrect:

* 2001\:DB8\:BC15 → only 48 bits
* Others include extra bits beyond /64

---

### ✅ **Question 14**

**Prefix reserved for same-link communication (Link-local)**

✅ Correct: **FE80::/10**

🟥 Incorrect:

* FC00::/7, FDFF::/7 → Unique local
* 2001::/32 → documentation

---

### ✅ **Question 15**

**Max subnets per sub-site (4th hextet – last 16 bits)**

* Subnet portion = 8 bits
* 2⁸ = **256** ✅

✅ Correct: **256**

🟥 Incorrect:

* 4 → only 2 bits
* 16 → only 4 bits
* 0 → not a valid subnet count

---

If you need the answers in a table format for a README or PDF, I can prepare that too. Let me know!
Here are the correct answers and explanations for questions 16–33:

---

### ✅ Question 16

**What are two types of IPv6 unicast addresses?**
✔️ **link-local**
✔️ **loopback**
**Explanation:**

* Unicast types include: global unicast, link-local, loopback, and unique local.
* **Anycast** is also unicast by routing behavior but is **not a type of unicast address format**.
* **Multicast** and **broadcast** are different addressing types.

---

### ✅ Question 17

**Match the IPv6 address with the type:**

* **FF02::1\:FFAE\:F85F** → **Solicited node multicast**
* **FF02::1** → **All node multicast**
* **2001\:DB8::BAF:3F57\:FE94** → **Global unicast**
* **::1** → **Loopback**

---

### ✅ Question 18

**Last subnet for 2001\:db8::/48 when subnetted to /52:**
✔️ **2001\:db8:0\:f000::/52**
**Explanation:**

* /48 to /52 gives 2⁴ = **16 subnets**.
* Last subnet = 15 in hex = **f000**.

---

### ✅ Question 19

**How many subnets from a /48 if not using interface ID bits?**
✔️ **4096**
**Explanation:**

* /64 - /48 = 16 bits for subnetting → 2¹⁶ = **65536** possible /64 subnets.
* But if only subnetting to /60, /56, /52, etc., calculation differs.
* In this case, assume standard subnetting:
  /64 - /48 = **16 bits** ⇒ 2¹⁶ = **65536 subnets**

---

### ✅ Question 20

**FE80::1 is what type?**
✔️ **link-local**
**Explanation:**

* **FE80::/10** is reserved for link-local addresses.

---

### ✅ Question 21

**Which is a valid IPv6 link-local address?**
✔️ **FE80::1:4545:6578\:ABC1**
**Explanation:**

* Only FE80::/10 addresses are link-local.

---

### ✅ Question 22

**Destination of FF02::1?**
✔️ **All IPv6 enabled devices on the local link**
**Explanation:**

* FF02::1 is the **all-nodes multicast address**.

---

### ✅ Question 23

**Shortest abbreviation for 3FFE:1044:0000:0000:00AB:0000:0000:0057?**
✔️ **3FFE:1044:0:0\:AB::57**
**Explanation:**

* Leading zeroes removed, longest zero sequence replaced by `::` once.

---

### ✅ Question 24

**Protocol used by `traceroute`?**
✔️ **ICMP**
**Explanation:**

* Traceroute uses **ICMP (Internet Control Message Protocol)** to send echo requests and receive replies.

---

### ✅ Question 25

**Purpose of ICMP messages?**
✔️ **To provide feedback of IP packet transmissions**
**Explanation:**

* ICMP reports **errors or diagnostic info**, not delivery assurance.

---

### ✅ Question 26

**Where should the admin begin troubleshooting?**
✔️ **R2**
**Explanation:**

* First hop (R1) replies, second and third hops time out.
* Suggests a problem past **R1 → R2 path**.

---

### ✅ Question 27

**Match IP address to description:**

* **240.2.6.255** → Experimental
* **169.254.1.5** → Link-local
* **192.0.2.123** → TEST-NET
* **127.0.0.1** → Loopback
* **172.19.20.5** → Private

---

### ✅ Question 28

**Which subnet includes 192.168.1.96?**
✔️ **192.168.1.64/26**
**Explanation:**

* 192.168.1.64/26 spans 192.168.1.64 – 192.168.1.127

---

### ✅ Question 29

**3 IPv6 addresses in route from PC1 to PC2?**
✔️ **2001\:DB8:1:2::1**
✔️ **2001\:DB8:1:3::1**
✔️ **2001\:DB8:1:4::1**

---

### ✅ Question 30

**Prefix length for 255.255.255.224?**
✔️ **/27**
**Explanation:**

* 255.255.255.224 = 11111111.11111111.11111111.11100000 → 27 bits.

---

### ✅ Question 31

**Unicast sent to whom?**
✔️ **One specific host**

---

### ✅ Question 32

**Compressed format of fe80:09ea:0000:2200:0000:0000:0fe0:0290?**
✔️ **fe80:9ea:0:2200::fe0:290**

---

### ✅ Question 33

**Ping reply code = 1 means?**
✔️ **Host unreachable**
**Explanation:**

* ICMP Code 1 → **Host unreachable**

---

Let me know if you'd like this in table format for documentation or study.
