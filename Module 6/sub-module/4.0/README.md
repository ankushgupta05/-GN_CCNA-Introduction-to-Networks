Here are the answers to **6.4.2 Module Quiz – Data Link Layer** formatted with options, correct answers, and explanations:

---

### **Question 1**

**What identifier is used at the data link layer to uniquely identify an Ethernet device?**

| Option             | Answer      | Explanation                                               |
| ------------------ | ----------- | --------------------------------------------------------- |
| 🅐 IP address      | ❌ Incorrect | IP addresses operate at the network layer (Layer 3).      |
| 🅑 MAC address     | ✅ Correct   | MAC addresses are Layer 2 identifiers unique to each NIC. |
| 🅒 Sequence number | ❌ Incorrect | Sequence numbers are part of the transport layer.         |
| 🅓 TCP port number | ❌ Incorrect | Port numbers are used at Layer 4.                         |
| 🅔 UDP port number | ❌ Incorrect | Same as above – these are transport layer concepts.       |

---

### **Question 2**

**What attribute of a NIC would place it at the data link layer of the OSI model?**

| Option                     | Answer      | Explanation                                                 |
| -------------------------- | ----------- | ----------------------------------------------------------- |
| 🅐 Attached Ethernet cable | ❌ Incorrect | This relates to the physical layer.                         |
| 🅑 IP address              | ❌ Incorrect | IP addresses operate at the network layer.                  |
| 🅒 MAC address             | ✅ Correct   | MAC addresses identify devices at the data link layer.      |
| 🅓 RJ-45 port              | ❌ Incorrect | This is a hardware interface related to the physical layer. |
| 🅔 TCP/IP protocol stack   | ❌ Incorrect | Refers to all layers, not just Layer 2.                     |

---

### **Question 3**

**Which two engineering organizations define open standards and protocols that apply to the data link layer? (Choose two.)**

| Option                                                      | Answer      | Explanation                                                                        |
| ----------------------------------------------------------- | ----------- | ---------------------------------------------------------------------------------- |
| 🅐 Institute of Electrical and Electronics Engineers (IEEE) | ✅ Correct   | IEEE defines Layer 2 standards like Ethernet (IEEE 802.3) and Wi-Fi (IEEE 802.11). |
| 🅑 Internet Assigned Numbers Authority (IANA)               | ❌ Incorrect | IANA manages IP addresses and DNS at higher layers.                                |
| 🅒 International Telecommunication Union (ITU)              | ✅ Correct   | ITU defines telecom standards, including some Layer 2 protocols.                   |
| 🅓 Electronic Industries Alliance (EIA)                     | ❌ Incorrect | EIA deals more with physical layer standards.                                      |
| 🅔 Internet Society (ISOC)                                  | ❌ Incorrect | ISOC supports internet growth and policies, not specifically Layer 2.              |

---

### **Question 4**

**What is true concerning physical and logical topologies?**

| Option                                                                       | Answer      | Explanation                          |
| ---------------------------------------------------------------------------- | ----------- | ------------------------------------ |
| 🅐 The logical topology is always the same as the physical topology.         | ❌ Incorrect | They can differ.                     |
| 🅑 Physical topologies are concerned with how a network transfers frames.    | ❌ Incorrect | Logical topologies describe this.    |
| 🅒 Physical topologies display the IP addressing scheme of each network.     | ❌ Incorrect | IP addressing is a Layer 3 function. |
| 🅓 Logical topologies refer to how a network transfers data between devices. | ✅ Correct   | This defines the data flow path.     |

---

### **Question 5**

**What method is used to manage contention-based access on a wireless network?**

| Option               | Answer      | Explanation                                           |
| -------------------- | ----------- | ----------------------------------------------------- |
| 🅐 CSMA/CD           | ❌ Incorrect | Used in wired Ethernet, not wireless.                 |
| 🅑 Priority ordering | ❌ Incorrect | Not a standard contention-based method.               |
| 🅒 CSMA/CA           | ✅ Correct   | Wireless networks use CSMA/CA to avoid collisions.    |
| 🅓 Token passing     | ❌ Incorrect | Used in older deterministic networks like Token Ring. |

---

### **Question 6**

**Which physical topology requires that every node is attached to every other node on the network?**

| Option          | Answer      | Explanation                                           |
| --------------- | ----------- | ----------------------------------------------------- |
| 🅐 Bus          | ❌ Incorrect | All devices share a single communication line.        |
| 🅑 Hierarchical | ❌ Incorrect | Not a mesh; uses levels of control.                   |
| 🅒 Mesh         | ✅ Correct   | In a full mesh, every device connects to every other. |
| 🅓 Ring         | ❌ Incorrect | Devices are connected in a circular path.             |
| 🅔 Star         | ❌ Incorrect | Devices connect to a central hub or switch.           |

---

### **Question 7**

**Which statement describes the half-duplex mode of data transmission?**

| Option                                                                                                             | Answer      | Explanation                                                       |
| ------------------------------------------------------------------------------------------------------------------ | ----------- | ----------------------------------------------------------------- |
| 🅐 Data that is transmitted over the network can only flow in one direction.                                       | ❌ Incorrect | That describes simplex.                                           |
| 🅑 Data that is transmitted over the network flows in one direction at a time.                                     | ✅ Correct   | Half-duplex allows two-way communication, but not simultaneously. |
| 🅒 Data that is transmitted over the network flows in one direction to many different destinations simultaneously. | ❌ Incorrect | This resembles broadcast, not half-duplex.                        |
| 🅓 Data that is transmitted over the network flows in both directions at the same time.                            | ❌ Incorrect | That’s full-duplex.                                               |

---

### **Question 8**

**Which is a function of the Logical Link Control (LLC) sublayer?**

| Option                                                                         | Answer      | Explanation                                    |
| ------------------------------------------------------------------------------ | ----------- | ---------------------------------------------- |
| 🅐 To define the media access processes that are performed by the hardware     | ❌ Incorrect | This is done by the MAC sublayer.              |
| 🅑 To provide data link layer addressing                                       | ❌ Incorrect | MAC sublayer handles addressing.               |
| 🅒 To identify which network layer protocol is being used                      | ✅ Correct   | LLC identifies Layer 3 protocols in the frame. |
| 🅓 To accept segments and package them into data units that are called packets | ❌ Incorrect | That’s the network layer’s role.               |

---

### **Question 9**

**Which data link layer media access control method does Ethernet use with legacy Ethernet hubs?**

| Option           | Answer      | Explanation                                           |
| ---------------- | ----------- | ----------------------------------------------------- |
| 🅐 CSMA/CD       | ✅ Correct   | Ethernet with hubs uses CSMA/CD to detect collisions. |
| 🅑 Determinism   | ❌ Incorrect | Ethernet is not deterministic.                        |
| 🅒 Turn taking   | ❌ Incorrect | This describes methods like polling, not Ethernet.    |
| 🅓 Token passing | ❌ Incorrect | Not used in Ethernet, only in Token Ring.             |

---

### **Question 10**

**What are the two sublayers of the OSI model data link layer? (Choose two.)**

| Option            | Answer      | Explanation                                            |
| ----------------- | ----------- | ------------------------------------------------------ |
| 🅐 Internet       | ❌ Incorrect | Not a sublayer, this is part of the network layer.     |
| 🅑 Physical       | ❌ Incorrect | It is a separate layer, not a sublayer of Layer 2.     |
| 🅒 LLC            | ✅ Correct   | Logical Link Control is the upper sublayer of Layer 2. |
| 🅓 Transport      | ❌ Incorrect | This is Layer 4.                                       |
| 🅔 MAC            | ✅ Correct   | Media Access Control is the lower sublayer of Layer 2. |
| 🅕 Network access | ❌ Incorrect | This is a TCP/IP model term, not an OSI sublayer.      |

---

### **Question 11**

**Which layer of the OSI model is responsible for specifying the encapsulation method used for specific types of media?**

| Option         | Answer      | Explanation                                  |
| -------------- | ----------- | -------------------------------------------- |
| 🅐 Application | ❌ Incorrect | Deals with user interface and services.      |
| 🅑 Transport   | ❌ Incorrect | Provides reliable delivery of data.          |
| 🅒 Data link   | ✅ Correct   | Specifies framing and encapsulation methods. |
| 🅓 Physical    | ❌ Incorrect | Deals with transmission of raw bits.         |

---

### **Question 12**

**What type of physical topology can be created by connecting all Ethernet cables to a central device?**

| Option  | Answer      | Explanation                                     |
| ------- | ----------- | ----------------------------------------------- |
| 🅐 Bus  | ❌ Incorrect | Uses a single shared backbone.                  |
| 🅑 Ring | ❌ Incorrect | Devices connect in a closed loop.               |
| 🅒 Star | ✅ Correct   | All devices connect to a central switch or hub. |
| 🅓 Mesh | ❌ Incorrect | Each device connects to every other device.     |

---

### **Question 13**

**What are two services performed by the data link layer of the OSI model? (Choose two.)**

| Option                                                                    | Answer      | Explanation                                            |
| ------------------------------------------------------------------------- | ----------- | ------------------------------------------------------ |
| 🅐 It fragments data packets into the MTU size.                           | ❌ Incorrect | This is done at the network layer.                     |
| 🅑 It determines the path to forward packets.                             | ❌ Incorrect | This is the role of routers at Layer 3.                |
| 🅒 It accepts Layer 3 packets and encapsulates them into frames.          | ✅ Correct   | Layer 2 encapsulates packets into frames.              |
| 🅓 It provides media access control and performs error detection.         | ✅ Correct   | Media access and error checking are Layer 2 tasks.     |
| 🅔 It monitors the Layer 2 communication by building a MAC address table. | ❌ Incorrect | This is done by switches, not by the OSI model itself. |

---

### **Question 14**

**Although CSMA/CD is still a feature of Ethernet, why is it no longer necessary?**

| Option                                                    | Answer      | Explanation                                                       |
| --------------------------------------------------------- | ----------- | ----------------------------------------------------------------- |
| 🅐 The virtually unlimited availability of IPv6 addresses | ❌ Incorrect | Not related to data collisions.                                   |
| 🅑 The use of CSMA/CA                                     | ❌ Incorrect | CSMA/CA is for wireless networks.                                 |
| 🅒 The use of full-duplex capable Layer 2 switches        | ✅ Correct   | Full-duplex eliminates collisions, making CSMA/CD unnecessary.    |
| 🅓 The development of half-duplex switch operation        | ❌ Incorrect | Half-duplex still allows collisions.                              |
| 🅔 The use of Gigabit Ethernet speeds                     | ❌ Incorrect | While faster, speed doesn’t eliminate the need for CSMA/CD alone. |

---

Let me know if you'd like this exported to a table for a README or quiz review sheet.
