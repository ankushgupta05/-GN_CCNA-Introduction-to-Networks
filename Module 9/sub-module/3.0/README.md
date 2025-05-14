Here’s a concise summary of **IPv6 Neighbor Discovery (ND)** based on the content you shared:

---

### ✅ **9.3.1 – IPv6 Neighbor Discovery Overview**

* **ND (Neighbor Discovery)** in IPv6 is the replacement for ARP in IPv4.
* ND matches IPv6 addresses to MAC addresses.
* It uses **ICMPv6 messages** to provide services like:

  * Address resolution
  * Router discovery
  * Redirection

---

### ✅ **9.3.2 – ND Message Types (ICMPv6)**

ND uses **five types of ICMPv6 messages**:

| **Message**            | **Purpose**                                             |
| ---------------------- | ------------------------------------------------------- |
| Neighbor Solicitation  | Sent by a device to discover the MAC of another device  |
| Neighbor Advertisement | Response containing MAC address of requested device     |
| Router Solicitation    | Sent by host to request router info                     |
| Router Advertisement   | Sent by router with info like network prefix, gateway   |
| Redirect               | Suggests better next-hop router (not covered in detail) |

> 💡 **Note:** ND works at **Layer 3 (Network Layer)** and uses **multicast** instead of broadcast like ARP.

---

### ✅ **9.3.3 – ND for Address Resolution (ARP Equivalent in IPv6)**

#### 🔁 **How Address Resolution Works in IPv6:**

1. **PC1** wants to reach **PC2** with IPv6 `2001:db8:acad:1::11`.
2. PC1 sends an **ICMPv6 Neighbor Solicitation**:

   > “Hey whoever has `2001:db8:acad:1::11`, send me your MAC address?”
3. **PC2** receives it and sends an **ICMPv6 Neighbor Advertisement**:

   > “Hey `2001:db8:acad:1::10`, I am `2001:db8:acad:1::11` and my MAC address is `f8-94-c3-e4-c5-0A`.”

#### 📌 Key Differences from ARP:

* **Multicast** (not broadcast) is used for discovery.
* Uses **ICMPv6 messages**, not standalone ARP protocol.
* Devices process messages more efficiently using **special Ethernet filters**.

---

Here are the correct answers for **9.3.5 Check Your Understanding - Neighbor Discovery**:

---

### ✅ **Question 1: Which two ICMPv6 messages are used in SLAAC?**

✔️ **Router Advertisement**
✔️ **Router Solicitation**

> **Explanation:**
> SLAAC (Stateless Address Autoconfiguration) uses *Router Solicitation* to ask for configuration, and *Router Advertisement* to receive it from the router.

---

### ✅ **Question 2: Which two ICMPv6 messages are used to determine the MAC address of a known IPv6 address?**

✔️ **Neighbor Solicitation**
✔️ **Neighbor Advertisement**

> **Explanation:**
> These two are used like ARP in IPv4:

* A device sends a *Neighbor Solicitation* to ask who owns an IPv6 address.
* The device with that address replies with a *Neighbor Advertisement* containing its MAC address.

---

### ✅ **Question 3: To what type of address are ICMPv6 neighbor solicitation messages sent?**

✔️ **Multicast**

> **Explanation:**
> IPv6 ND uses **multicast**, not broadcast like ARP. This is more efficient and reduces unnecessary load on other hosts.

---

Let me know if you'd like these added to a markdown study sheet or visual summary!
