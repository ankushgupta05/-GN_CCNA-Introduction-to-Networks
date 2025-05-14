Here are the **correct answers** for **9.4.2 Module Quiz - Address Resolution**, along with brief explanations:

---

### ✅ **Question 1:**

**Which router component holds the routing table, ARP cache, and running configuration file?**
✔️ **RAM**

> RAM stores volatile data such as the routing table, ARP cache, and running config.

---

### ✅ **Question 2:**

**What type of information is contained in an ARP table?**
✔️ **IPv4 address to MAC address mappings**

> ARP maps known IPv4 addresses to their corresponding MAC addresses.

---

### ✅ **Question 3:**

**What does the ARP entry 192.168.1.255 ff-ff-ff-ff-ff-ff represent?**
✔️ **This is a dynamic map entry.**

> This entry shows a broadcast IP address mapped to the broadcast MAC address, which typically appears dynamically.

---

### ✅ **Question 4:**

**Which command shows the MAC address a host uses to reach the default gateway?**
✔️ **arp -a**

> Displays the ARP table showing IP-to-MAC address mappings.

---

### ✅ **Question 5:**

**What will a Layer 2 switch do when the destination MAC is unknown?**
✔️ **It forwards the frame out of all ports except for the port at which the frame was received.**

> This is called **flooding**, a default behavior when the MAC is not in the table.

---

### ✅ **Question 6:**

**Which two ICMPv6 messages are used during the MAC address resolution process?**
✔️ **Neighbor Solicitation**
✔️ **Neighbor Advertisement**

> These perform the function of ARP in IPv6.

---

### ✅ **Question 7:**

**How does ARP use an IPv4 address?**
✔️ **To determine the MAC address of a device on the same network**

> ARP resolves the MAC of local IPv4 addresses only.

---

### ✅ **Question 8:**

**What is one function of the ARP protocol?**
✔️ **Resolving an IPv4 address to a MAC address**

> That’s ARP’s main job.

---

### ✅ **Question 9:**

**What does a Layer 2 switch do with a broadcast frame?**
✔️ **It sends the frame to all ports.**

> Broadcast frames are forwarded to all switch ports.

---

### ✅ **Question 10:**

**What addresses are mapped by ARP?**
✔️ **IPv4 address to a destination MAC address**

> ARP provides this mapping to allow communication over Ethernet.

---

### ✅ **Question 11:**

**What does ARP provide when sending a packet to a remote network?**
✔️ **The MAC address of the router interface closest to the sending host**

> The sender uses ARP to get the MAC address of the default gateway.

---

### ✅ **Question 12:**

**What two types of address are mapped in the ARP table?**
✔️ **Layer 3 address to a Layer 2 address**

> IP address (Layer 3) ↔ MAC address (Layer 2).

---

### ✅ **Question 13:**

**What is the purpose of ARP in IPv4 networks?**
✔️ **To obtain a specific MAC address when an IP address is known**

> ARP resolves IP to MAC to complete frame delivery on Ethernet.

---

### ✅ **Question 14:**

**Which destination address is used in an ARP request frame?**
✔️ **FFFF.FFFF.FFFF**

> This is the **broadcast MAC address** used in ARP requests.

---

Let me know if you'd like this in a table or Markdown format for documentation or studying!
