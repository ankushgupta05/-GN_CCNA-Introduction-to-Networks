Here are the **correct answers** to the **12.9.4 Module Quiz - IPv6 Addressing**, with detailed **explanations** on **why each option is correct or incorrect**:

---

### ✅ **Question 1**

**Q:** What is the valid most compressed format possible of the IPv6 address `2001:0DB8:0000:AB00:0000:0000:0000:1234`?

| Option                     | Answer        | Explanation                                                                       |
| -------------------------- | ------------- | --------------------------------------------------------------------------------- |
| 🔘 `2001:DB8:0:AB00::1234` | ✅ **Correct** | `::` replaces the **longest contiguous block** of zero groups (`0000:0000:0000`). |
| `2001:DB8:0:AB::1234`      | ❌ Incorrect   | `AB00` ≠ `AB`, this changes the value of the original address.                    |
| `2001:DB8::AB00::1234`     | ❌ Incorrect   | Invalid syntax – `::` can **only appear once** in an address.                     |
| `2001:DB8:0:AB:0:1234`     | ❌ Incorrect   | Loses too many groups, and not properly zero-compressed.                          |

---

### ✅ **Question 2**

**Q:** What is the prefix associated with the IPv6 address `2001:DB8:D15:EA:CC44::1/64`?

| Option                      | Answer        | Explanation                                                          |
| --------------------------- | ------------- | -------------------------------------------------------------------- |
| `2001::/64`                 | ❌ Incorrect   | This is too broad; it only includes the first 16 bits.               |
| `2001:DB8::/64`             | ❌ Incorrect   | Still too short; it only covers up to the first 32 bits.             |
| ✅ `2001:DB8:D15:EA::/64`    | ✅ **Correct** | A `/64` prefix includes the **first 4 hextets**.                     |
| `2001:DB8:D15:EA:CC44::/64` | ❌ Incorrect   | Too long—`CC44` is part of the interface ID, not the network prefix. |

---

### ✅ **Question 3**

**Q:** What type of address is automatically assigned to an interface when IPv6 is enabled on that interface?

| Option           | Answer        | Explanation                                                              |
| ---------------- | ------------- | ------------------------------------------------------------------------ |
| `Global unicast` | ❌ Incorrect   | These must be assigned manually or via DHCPv6.                           |
| ✅ `Link-local`   | ✅ **Correct** | **Automatically generated** when IPv6 is enabled (starts with `FE80::`). |
| `Loopback`       | ❌ Incorrect   | `::1` is the loopback, used **only for testing the local device**.       |
| `Unique local`   | ❌ Incorrect   | Private-like IPv6 addresses (`FC00::/7`), not auto-assigned.             |

---

### ✅ **Question 4**

**Q:** Which IPv6 network prefix is only intended for local links and cannot be routed?

| Option        | Answer        | Explanation                                                             |
| ------------- | ------------- | ----------------------------------------------------------------------- |
| `2001::/3`    | ❌ Incorrect   | This includes globally routable addresses.                              |
| `FC00::/7`    | ❌ Incorrect   | Unique Local Addresses – **private**, but **can be routed internally**. |
| ✅ `FE80::/10` | ✅ **Correct** | **Link-local addresses**, not routable beyond the local link.           |
| `FF00::/12`   | ❌ Incorrect   | Multicast addresses, not intended for link-local only.                  |

---

### ✅ **Question 5**

**Q:** What is the purpose of the command `ping ::1`?

| Option                                                              | Answer        | Explanation                                                          |
| ------------------------------------------------------------------- | ------------- | -------------------------------------------------------------------- |
| ✅ `It tests the internal configuration of an IPv6 host.`            | ✅ **Correct** | `::1` is the IPv6 **loopback address**, used to test local IP stack. |
| `It tests the broadcast capability of all hosts on the subnet.`     | ❌ Incorrect   | IPv6 **does not use broadcast**.                                     |
| `It tests the multicast connectivity to all hosts on the subnet.`   | ❌ Incorrect   | That would involve `ff02::1`.                                        |
| `It tests the reachability of the default gateway for the network.` | ❌ Incorrect   | That would involve pinging the gateway address, not `::1`.           |

---

### ✅ **Question 6**

**Q:** What is the interface ID of the IPv6 address `2001:DB8::1000:A9CD:47FF:FE57:FE94/64`?

| Option                       | Answer        | Explanation                                                   |
| ---------------------------- | ------------- | ------------------------------------------------------------- |
| `FE94`                       | ❌ Incorrect   | Just the last 16 bits; **too short**.                         |
| `FE57:FE94`                  | ❌ Incorrect   | Still not full 64-bit interface ID.                           |
| `47FF:FE57:FE94`             | ❌ Incorrect   | Partial—missing the start of the Interface ID.                |
| ✅ `1000:A9CD:47FF:FE57:FE94` | ✅ **Correct** | After `/64`, the **remaining 64 bits** form the Interface ID. |
| `A9CD:47FF:FE57:FE94`        | ❌ Incorrect   | 64 bits, yes—but missing the `1000` at the beginning.         |

---

### ✅ **Question 7**

**Q:** What is the network address for the IPv6 address `2001:DB8:AA04:B5::1/64`?

| Option                    | Answer        | Explanation                                              |
| ------------------------- | ------------- | -------------------------------------------------------- |
| `2001::/64`               | ❌ Incorrect   | Only includes the first 16 bits; too general.            |
| `2001:DB8::/64`           | ❌ Incorrect   | Only includes the first 32 bits.                         |
| `2001:DB8:AA04::/64`      | ❌ Incorrect   | Only includes the first 48 bits; **not enough** for /64. |
| ✅ `2001:DB8:AA04:B5::/64` | ✅ **Correct** | **First 64 bits** form the network portion.              |

---

### 🧾 Summary Table

| Question | Correct Option                                           | Why Selected                                |
| -------- | -------------------------------------------------------- | ------------------------------------------- |
| Q1       | ✅ `2001:DB8:0:AB00::1234`                                | Proper compression of longest zero sequence |
| Q2       | ✅ `2001:DB8:D15:EA::/64`                                 | First 64 bits = 4 hextets                   |
| Q3       | ✅ `Link-local`                                           | Auto-assigned upon enabling IPv6            |
| Q4       | ✅ `FE80::/10`                                            | Link-local, not routable                    |
| Q5       | ✅ `It tests the internal configuration of an IPv6 host.` | `::1` = loopback                            |
| Q6       | ✅ `1000:A9CD:47FF:FE57:FE94`                             | Last 64 bits = Interface ID                 |
| Q7       | ✅ `2001:DB8:AA04:B5::/64`                                | First 64 bits = Network address             |

Let me know if you want this turned into a printable quiz with answers and explanations!


Here are the **correct answers with explanations** for questions 8–15 of your IPv6 module quiz:

---

### **Question 8**

**Which address type is not supported in IPv6?**

✅ **Correct Answer:** `Broadcast`

🔍 **Explanation:**
IPv6 does **not use broadcast addresses**. Instead, it uses **multicast** to communicate with multiple hosts.

* **Unicast:** Supported
* **Multicast:** Supported
* **Private (Unique local):** Supported
* **Broadcast:** ❌ Not supported in IPv6

---

### **Question 9**

**What is indicated by a successful ping to the ::1 IPv6 address?**

✅ **Correct Answer:** `IP is properly installed on the host.`

🔍 **Explanation:**
`::1` is the **loopback address** in IPv6. A successful ping means the **IPv6 stack is functioning properly** on the local machine.
It **does not** test cable, gateway, or link-local connectivity.

---

### **Question 10**

**What is the most compressed representation of the IPv6 address `2001:0db8:0000:abcd:0000:0000:0000:0001`?**

✅ **Correct Answer:** `2001:db8:0:abcd::1`

🔍 **Explanation:**
Rules for compression:

* Leading 0s in any block can be removed.
* One sequence of consecutive 0 blocks can be replaced with `::` (only once).

Original:
`2001:0db8:0000:abcd:0000:0000:0000:0001` →
Remove leading 0s: `2001:db8:0:abcd:0:0:0:1` →
Compress longest 0s: `2001:db8:0:abcd::1`

---

### **Question 11**

**What is the minimum configuration for a router interface that is enabled for IPv6?**

✅ **Correct Answer:** `To have a link-local IPv6 address`

🔍 **Explanation:**
IPv6-enabled interfaces **automatically generate a link-local address**, which is **required** and sufficient for basic communication like neighbor discovery.
Global addresses are not mandatory unless external communication is needed.

---

### **Question 12**

**At a minimum, which address is required on IPv6-enabled interfaces?**

✅ **Correct Answer:** `Link-local`

🔍 **Explanation:**
Link-local addresses (starting with `FE80::/10`) are **mandatory** for all IPv6 interfaces. They're used for **local communication** like routing protocols, discovery, etc.
Other types (unique local, global) are optional.

---

### **Question 13**

**What are three parts of an IPv6 global unicast address? (Choose three.)**

✅ **Correct Answers:**

* `A global routing prefix that is used to identify the network portion of the address that has been provided by an ISP`
* `A subnet ID that is used to identify networks inside of the local enterprise site`
* `An interface ID that is used to identify the local host on the network`

🔍 **Explanation:**
A global unicast address has the following structure:
`[Global Routing Prefix (assigned by ISP)] + [Subnet ID] + [Interface ID]`
Used for uniquely identifying hosts on the internet.

---

### **Question 14**

**Your organization is issued the IPv6 prefix of `2001:db8:130f::/48` by your service provider. With this prefix, how many bits are available for your organization to create /64 subnetworks if interface ID bits are not borrowed?**

✅ **Correct Answer:** `16`

🔍 **Explanation:**

* IPv6 address: 128 bits
* /48 prefix → 48 bits fixed by ISP
* /64 subnets → 64 bits required
* So, **64 − 48 = 16 bits** available for subnetting
  Your organization can create **2^16 = 65,536** /64 subnets.

---

### **Question 15**

**Which type of IPv6 address is not routable and used only for communication on a single subnet?**

✅ **Correct Answer:** `Link-local address`

🔍 **Explanation:**

* **Link-local addresses** (`FE80::/10`) are used **only for communication on the local link** (single subnet), such as neighbor discovery and routing.
* They are **not routable** beyond the link.
* Other addresses (global, unique local) **can be routed** within limits.

---

Let me know if you’d like a **summary table** for all questions 1–15.
