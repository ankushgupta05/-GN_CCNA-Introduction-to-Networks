# note :- 32 wrong  answer hai

Here are the **correct answers with explanations** for each question of your quiz:

---

### 📘 Module Quiz – Network Layer (IPv4, IPv6, ARP, etc.)

| Q# | Question                                                                                              | Correct Answer                                                                                               | Explanation                                                                                            |
| -- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| 1  | What IPv4 header field identifies the upper layer protocol carried in the packet?                     | ✅ **Protocol**                                                                                               | The `Protocol` field in the IPv4 header indicates the next-level protocol (e.g., TCP, UDP).            |
| 2  | What information does the loopback test provide?                                                      | ✅ **The TCP/IP stack on the device is working correctly.**                                                   | Loopback test (`ping 127.0.0.1`) verifies if the TCP/IP stack is functioning on the device.            |
| 3  | Which statement describes a feature of the IP protocol?                                               | ✅ **IP relies on upper layer services to handle situations of missing or out-of-order packets.**             | IP is a connectionless protocol and doesn't ensure reliability; that’s handled by TCP.                 |
| 4  | What is one advantage that the IPv6 simplified header offers over IPv4?                               | ✅ **efficient packet handling**                                                                              | IPv6 has a simplified header to improve processing efficiency in routers.                              |
| 5  | Which field in the IPv4 header is used to prevent a packet from traversing a network endlessly?       | ✅ **Time-to-Live**                                                                                           | TTL limits the lifetime of a packet to prevent infinite loops.                                         |
| 6  | What are two services provided by the OSI network layer?                                              | ✅ **encapsulating PDUs from the transport layer**<br>✅ **routing packets toward the destination**            | Network layer encapsulates and routes packets to their destinations.                                   |
| 7  | What is the purpose of configuring a switch with a default gateway address?                           | ✅ **The default gateway address is used to forward packets originating from the switch to remote networks.** | It's used when the switch (e.g., for remote management) needs to reach outside networks.               |
| 8  | Which parameter does the router use to choose the path to the destination when multiple routes exist? | ✅ **the lower metric value that is associated with the destination network**                                 | Routers prefer paths with the **lowest metric** (e.g., cost, hop count).                               |
| 9  | A computer can access devices on the same network but not others. What’s the probable cause?          | ✅ **The computer has an invalid default gateway address.**                                                   | Without a correct default gateway, packets to other networks cannot be routed.                         |
| 10 | What is the aim of an ARP spoofing attack?                                                            | ✅ **to associate IP addresses to the wrong MAC address**                                                     | ARP spoofing tricks devices into associating the wrong MAC with an IP address.                         |
| 11 | PC1 sends an ARP request to connect to File\_server1. Which MAC will it receive?                      | ✅ **the MAC address of the G0/0 interface on R1**                                                            | Since File\_server1 is on a remote network, PC1 sends the packet to R1, so ARP resolves R1's G0/0 MAC. |
| 12 | How are ARP requests treated on the local link?                                                       | ✅ **They are received and processed by every device on the local network.**                                  | ARP requests are broadcast to all devices on the local subnet.                                         |
| 13 | What does `arp -d *` do on a PC?                                                                      | ✅ **The ARP cache is cleared.**                                                                              | This command removes all dynamic entries from the ARP table.                                           |
| 14 | What does a Layer 2 device examine in the Ethernet frame header?                                      | ✅ **destination MAC address**                                                                                | Switches use the **destination MAC** to forward frames at Layer 2.                                     |
| 15 | Where are IPv4-to-L2 Ethernet mappings maintained on a host?                                          | ✅ **ARP cache**                                                                                              | The ARP cache stores IP-to-MAC mappings on the device.                                                 |

---

Let me know if you'd like this exported as a `.md` file or formatted for a document/report.




Sure! Below are the answers with their corresponding questions from **Question 16 to Question 27**, each followed by the correct option and explanation:

---

### **Question 16**

**Q:** PC1 (port 4) sends a frame to PC3 (port 2). Only MACs on ports 1 and 3 are in the MAC table.
**What will the switch do with the frame?**

**✅ Answer:** *The switch will forward the frame to all ports except port 4.*

**Explanation:**
The destination MAC (PC3) is not in the MAC table. The switch floods the frame to all ports except the one it came from (port 4).

---

### **Question 17**

**Q:** Match the configuration mode with the available command.

| **Mode**         | **Answer**                         |
| ---------------- | ---------------------------------- |
| R1(config)#      | interface fastethernet 0/0         |
| R1>              | enable                             |
| R1#              | copy running-config startup-config |
| R1(config-line)# | login                              |

---

### **Question 18**

**Q:** What is the effect of `ip default-gateway 172.16.100.1` on a switch?

**✅ Answer:** *The switch can be remotely managed from a host on another network.*

**Explanation:**
This command sets the default gateway for out-of-network management access.

---

### **Question 19**

**Q:** Match the commands to their functions.

| **Function**                       | **Command**                         |
| ---------------------------------- | ----------------------------------- |
| Configures a name on the router    | Router(config)# hostname CL1        |
| Provides security on the console   | Router(config-line)# password class |
| Displays a message after accessing | Router(config)# banner motd #       |

---

### **Question 20**

**Q:** What happens when `transport input ssh` is entered on switch vty lines?

**✅ Answer:** *Communication between the switch and remote users is encrypted.*

**Explanation:**
This command restricts remote access to SSH only, ensuring encrypted communication.

---

### **Question 21**

**Q:** Which three commands are used to set up secure console access? (Choose 3)

**✅ Answers:**

* ✔️ password cisco
* ✔️ login
* ✔️ line console 0

**Explanation:**
These commands configure and secure access via the console.

---

### **Question 22**

**Q:** What is a description of the default gateway 192.168.1.254 from PC1?

**✅ Answer:** *It is the IP address of the Router1 interface that connects the PC1 LAN to Router1.*

**Explanation:**
The default gateway must be a directly connected router interface on the same network as PC1.

---

### **Question 23**

**Q:** Which two are primary functions of a router? (Choose 2)

**✅ Answers:**

* ✔️ path selection
* ✔️ packet forwarding

**Explanation:**
Routers determine best paths and forward packets accordingly.

---

### **Question 24**

**Q:** Match the access method descriptions.

| **Description**                           | **Access Method** |
| ----------------------------------------- | ----------------- |
| Remote access method that uses encryption | SSH               |
| Unsecure remote access                    | Telnet            |
| Preferred out-of-band access method       | Console           |
| Remote access via a dialup connection     | AUX               |

---

### **Question 25**

**Q:** Fastest way to test if the banner is configured?

**✅ Answer:** *Exit privileged EXEC mode and press Enter.*

**Explanation:**
The banner displays when a user logs in or presses Enter at the prompt.

---

### **Question 26**

**Q:** Match phases to boot functions.

| **Boot Phase** | **Function**                                    |
| -------------- | ----------------------------------------------- |
| Phase 1        | perform the POST and load the bootstrap program |
| Phase 2        | locate and load the Cisco IOS software          |
| Phase 3        | locate and load the startup configuration file  |

---

### **Question 27**

**Q:** What does `copy running-config startup-config` do?

**✅ Answer:** *The contents of NVRAM will change.*

**Explanation:**
This command saves the current config (in RAM) to NVRAM to make it persistent after reboot.

---
Here are the correct answers with explanations for **Question 28 to Question 33**:

---

### **Question 28**

**Q:** What will happen if the default gateway address is incorrectly configured on a host?

**✅ Answer:** *The host cannot communicate with hosts in other networks.*

**Explanation:**
The default gateway is used to send packets to other networks. If it is incorrect, the host can still communicate within its local network but cannot reach external networks.

---

### **Question 29**

**Q:** Which interfaces in each router are active and operational? *(From PT Activity)*

Since the activity needs Packet Tracer simulation to verify, the correct answer depends on your configuration, but assuming standard configuration from Cisco labs:

**✅ Possible Answer (based on common configurations):**
*R1: G0/0 and S0/0/0*
*R2: G0/1 and S0/0/0*

**Explanation:**
These are the most typically used interfaces for inter-router connections and local area access in labs. You should verify this answer by running `show ip interface brief` on each router.

---

### **Question 30**

**Q:** What are two potential network problems that can result from ARP operation? (Choose two)

**✅ Answers:**

* ✔️ On large networks with low bandwidth, multiple ARP broadcasts could cause data communication delays.
* ✔️ Network attackers could manipulate MAC address and IP address mappings in ARP messages with the intent of intercepting network traffic.

**Explanation:**
Excessive ARP broadcasts can congest a network. Also, ARP spoofing/poisoning is a well-known attack method used to redirect traffic.

---

### **Question 31**

**Q:** Which term describes a field in the IPv4 packet header that contains a 32-bit binary value associated with an interface on the sending device?

**✅ Answer:** *Source IPv4 address*

**Explanation:**
The source IP address field contains the 32-bit IP of the device that originated the packet.

---

### **Question 32**

**Q:** What property of ARP causes the request to be flooded out all ports of a switch except for the port receiving the ARP request?

**✅ Answer:** *The destination MAC address FF-FF-FF-FF-FF-FF appears in the header of the Ethernet frame.*

**Explanation:**
ARP requests are broadcast, and the destination MAC address of a broadcast is FF-FF-FF-FF-FF-FF. Switches flood broadcasts out all ports except the incoming one.

---

### **Question 33**

**Q:** What IP address would be configured as the default gateway on the new host in the Payroll LAN?

**✅ Answer:** *10.27.14.148*

**Explanation:**
This is the IP address of the interface `gi0/0` on RTR1, which connects to the Payroll LAN. Hosts should use the router interface on their subnet as the default gateway.

---

Let me know if you want these compiled into a Markdown table or exported as a PDF study guide!
