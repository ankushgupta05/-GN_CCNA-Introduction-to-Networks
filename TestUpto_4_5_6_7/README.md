Here's the formatted quiz with correct answers and explanations:

---

### Question 1

**What are two characteristics of fiber-optic cable? (Choose two.)**

| Option                                                                                 | Answer      | Explanation                                                                       |
| -------------------------------------------------------------------------------------- | ----------- | --------------------------------------------------------------------------------- |
| 🅐 It is more expensive than UTP cabling is.                                           | ✅ Correct   | Fiber-optic cables cost more due to their complexity and installation needs.      |
| 🅑 It combines the technique of cancellation, shielding, and twisting to protect data. | ❌ Incorrect | That is true for UTP, not fiber.                                                  |
| 🅒 It typically contains 4 pairs of fiber-optic wires.                                 | ❌ Incorrect | Fiber cables typically use one or two strands, not twisted pairs.                 |
| 🅓 Each pair of cables is wrapped in metallic foil.                                    | ❌ Incorrect | This applies to STP cables, not fiber.                                            |
| 🅔 It is not affected by EMI or RFI.                                                   | ✅ Correct   | Fiber-optic cables use light, making them immune to electromagnetic interference. |

---

### Question 2

**Which three factors could influence the differences in throughput? (Choose three.)**

| Option                                                                                    | Answer      | Explanation                                                                      |
| ----------------------------------------------------------------------------------------- | ----------- | -------------------------------------------------------------------------------- |
| 🅐 the bandwidth of the WAN connection to the Internet                                    | ✅ Correct   | Limited WAN bandwidth reduces overall throughput.                                |
| 🅑 the reliability of the gigabit Ethernet infrastructure of the backbone                 | ✅ Correct   | Faulty or unreliable infrastructure can lower effective throughput.              |
| 🅒 the latency that is created by the number of network devices that the data is crossing | ✅ Correct   | More devices introduce delay, impacting throughput.                              |
| 🅓 the amount of traffic that is currently crossing the network                           | ✅ Correct   | Congestion can reduce available throughput.                                      |
| 🅔 the sophistication of the encapsulation method applied to the data                     | ❌ Incorrect | Encapsulation overhead has minimal impact.                                       |
| 🅕 the type of traffic that is crossing the network                                       | ❌ Incorrect | Throughput is affected more by volume and efficiency, not traffic type directly. |

---

### Question 4

**What two factors could interfere with UTP communication? (Choose two.)**

| Option                          | Answer      | Explanation                                                |
| ------------------------------- | ----------- | ---------------------------------------------------------- |
| 🅐 size of the network          | ❌ Incorrect | Network size doesn't directly affect cable signal quality. |
| 🅑 signal modulation technique  | ❌ Incorrect | Modulation relates to transmission tech, not interference. |
| 🅒 bandwidth                    | ❌ Incorrect | Bandwidth is not interference.                             |
| 🅓 crosstalk                    | ✅ Correct   | Crosstalk is interference caused by adjacent wires.        |
| 🅔 electromagnetic interference | ✅ Correct   | UTP is susceptible to EMI without proper shielding.        |

---

### Question 6

**What is a primary role of the Physical layer?**

| Option                                                 | Answer      | Explanation                                                 |
| ------------------------------------------------------ | ----------- | ----------------------------------------------------------- |
| 🅐 determine the path packets take                     | ❌ Incorrect | That’s the role of Layer 3 (Network).                       |
| 🅑 provide physical addressing                         | ❌ Incorrect | MAC addresses are part of Layer 2.                          |
| 🅒 create the signals that represent bits on the media | ✅ Correct   | The Physical layer handles the actual transmission of bits. |
| 🅓 control data access to the media                    | ❌ Incorrect | This is a function of the MAC sublayer of Layer 2.          |

---

### Question 7

**Which statement is true about CSMA/CD?**

| Option                                                                          | Answer      | Explanation                                                        |
| ------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------ |
| 🅐 Devices involved in a collision get priority after backoff                   | ❌ Incorrect | All devices use random backoff to avoid collision.                 |
| 🅑 When a device hears a carrier signal and transmits, a collision cannot occur | ❌ Incorrect | Collision can still happen if two devices transmit simultaneously. |
| 🅒 All network devices must listen before transmitting                          | ✅ Correct   | This is the core of Carrier Sense in CSMA/CD.                      |
| 🅓 A jamming signal causes only colliding devices to back off                   | ❌ Incorrect | All devices on the network can detect the jam signal.              |

---

### Question 8

**What occurs at the data link layer during encapsulation?**

| Option                              | Answer      | Explanation                              |
| ----------------------------------- | ----------- | ---------------------------------------- |
| 🅐 An IP address is added           | ❌ Incorrect | IP is added at Layer 3.                  |
| 🅑 The logical address is added     | ❌ Incorrect | Logical (IP) address is part of Layer 3. |
| 🅒 The physical address is added    | ✅ Correct   | MAC address is added at Layer 2.         |
| 🅓 The process port number is added | ❌ Incorrect | Port numbers are added at Layer 4.       |

---

### Question 9

**What is contained in the trailer of a data-link frame?**

| Option              | Answer      | Explanation                                                            |
| ------------------- | ----------- | ---------------------------------------------------------------------- |
| 🅐 logical address  | ❌ Incorrect | That’s in the header.                                                  |
| 🅑 error detection  | ✅ Correct   | The trailer contains a Frame Check Sequence (FCS) for error detection. |
| 🅒 physical address | ❌ Incorrect | MAC addresses are in the header.                                       |
| 🅓 data             | ❌ Incorrect | Data is not in the trailer.                                            |

---

### Question 10

**Which two fields/features help Ethernet determine if a frame is valid? (Choose two.)**

| Option                  | Answer      | Explanation                                                                 |
| ----------------------- | ----------- | --------------------------------------------------------------------------- |
| 🅐 source MAC address   | ❌ Incorrect | Used for learning, not frame validation.                                    |
| 🅑 CEF                  | ❌ Incorrect | Cisco Express Forwarding is a Layer 3 feature.                              |
| 🅒 Frame Check Sequence | ✅ Correct   | FCS verifies frame integrity.                                               |
| 🅓 minimum frame size   | ✅ Correct   | Ethernet frames must meet a minimum size (64 bytes) to be considered valid. |
| 🅔 auto-MDIX            | ❌ Incorrect | This is related to cable type detection, not frame validation.              |

---

### Question 11

**What type of communication rule is CSMA/CD?**

| Option                   | Answer      | Explanation                                 |
| ------------------------ | ----------- | ------------------------------------------- |
| 🅐 message encapsulation | ❌ Incorrect | Encapsulation defines how data is packaged. |
| 🅑 flow control          | ❌ Incorrect | Flow control manages transmission rate.     |
| 🅒 message encoding      | ❌ Incorrect | Encoding relates to signal representation.  |
| 🅓 access method         | ✅ Correct   | CSMA/CD defines how media is accessed.      |

---

### Question 12

**Which statement describes a characteristic of data link layer frame header fields?**

| Option                                             | Answer      | Explanation                                             |
| -------------------------------------------------- | ----------- | ------------------------------------------------------- |
| 🅐 Ethernet headers contain Layer 3 addresses      | ❌ Incorrect | Only MAC addresses are in Ethernet headers.             |
| 🅑 All include flow control and logical connection | ❌ Incorrect | Not all frame types have flow control.                  |
| 🅒 They vary depending on protocols                | ✅ Correct   | Frame headers differ by protocol (Ethernet, PPP, etc.). |
| 🅓 They include info on user apps                  | ❌ Incorrect | Application info is in upper layers.                    |

---

### Question 13

**Function of CRC in FCS field?**

| Option                             | Answer      | Explanation                                     |
| ---------------------------------- | ----------- | ----------------------------------------------- |
| 🅐 verify frame integrity          | ✅ Correct   | CRC detects errors in the frame.                |
| 🅑 verify physical address         | ❌ Incorrect | Not related to MAC addresses.                   |
| 🅒 verify logical address          | ❌ Incorrect | IP addresses are not checked by CRC.            |
| 🅓 compute checksum for data field | ❌ Incorrect | CRC is used for the whole frame, not just data. |

---

### Question 14

**Which WAN topology connects some, but not all, sites?**

| Option            | Answer      | Explanation                                               |
| ----------------- | ----------- | --------------------------------------------------------- |
| 🅐 hub and spoke  | ❌ Incorrect | Hub and spoke connects all sites through a central point. |
| 🅑 partial mesh   | ✅ Correct   | Only some nodes are interconnected for redundancy.        |
| 🅒 point-to-point | ❌ Incorrect | This connects only two sites.                             |
| 🅓 mesh           | ❌ Incorrect | All nodes are interconnected.                             |

---

### Question 15

**What are three basic parts of all frame types? (Choose three.)**

| Option        | Answer      | Explanation                                    |
| ------------- | ----------- | ---------------------------------------------- |
| 🅐 type field | ❌ Incorrect | Not in all frame types.                        |
| 🅑 header     | ✅ Correct   | Present in all frames, includes addressing.    |
| 🅒 data       | ✅ Correct   | The payload of the frame.                      |
| 🅓 CRC value  | ✅ Correct   | Used for error checking.                       |
| 🅔 trailer    | ✅ Correct   | Contains the FCS in Ethernet.                  |
| 🅕 MTU size   | ❌ Incorrect | MTU is not a frame component but a size limit. |

---

Here are the answers in the previous format (table style) with options, correct answers, and brief explanations:

---

### ✅ **Question 16**

**Which two statements describe features or functions of the logical link control sublayer in Ethernet standards? (Choose two.)**

| Option                                                                                          | Answer | Explanation                                                                  |
| ----------------------------------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------------- |
| Logical link control is implemented in software.                                                | ✅      | LLC is a software-based sublayer used for flow control and error management. |
| The LLC sublayer is responsible for the placement and retrieval of frames on and off the media. | ❌      | That function belongs to the MAC sublayer.                                   |
| The data link layer uses LLC to communicate with the upper layers of the protocol suite.        | ✅      | LLC provides an interface to the Network layer.                              |
| The LLC sublayer adds a header and a trailer to the data.                                       | ❌      | Only a header is added by LLC; trailers are handled by MAC.                  |
| Logical link control is specified in the IEEE 802.3 standard.                                   | ❌      | LLC is specified in IEEE 802.2.                                              |

---

### ✅ **Question 17**

**Which is a multicast MAC address?**

| Option            | Answer | Explanation                                  |
| ----------------- | ------ | -------------------------------------------- |
| 01-00-5E-00-00-03 | ✅      | Multicast MAC addresses begin with 01-00-5E. |
| 5C-26-0A-4B-19-3E | ❌      | This is a unicast MAC address.               |
| 00-26-0F-4B-00-3E | ❌      | This is a unicast MAC address.               |
| FF-FF-FF-FF-FF-FF | ❌      | This is a broadcast address.                 |

---

### ✅ **Question 18**

**When the store-and-forward method of switching is in use, what part of the Ethernet frame is used to perform an error check?**

| Option                                | Answer | Explanation                                                                      |
| ------------------------------------- | ------ | -------------------------------------------------------------------------------- |
| destination MAC address in the header | ❌      | Used for forwarding, not error checking.                                         |
| CRC in the trailer                    | ✅      | CRC (Cyclic Redundancy Check) is in the trailer and is used for error detection. |
| source MAC address in the header      | ❌      | Identifies sender, not for error checking.                                       |
| protocol type in the header           | ❌      | Indicates protocol type, not for checking errors.                                |

---

### ✅ **Question 19**

**What are two actions performed by a Cisco switch? (Choose two.)**

| Option                                                                             | Answer | Explanation                                                            |
| ---------------------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------- |
| forwarding frames with unknown destination IP addresses to the default gateway     | ❌      | Switches operate at Layer 2 and use MAC addresses, not IP.             |
| using the source MAC addresses of frames to build and maintain a MAC address table | ✅      | Switches learn MAC addresses from the source field of incoming frames. |
| utilizing the MAC address table to forward frames via the destination MAC address  | ✅      | Switches use the MAC table to decide where to forward frames.          |
| building a routing table that is based on the first IP address in the frame header | ❌      | Routing tables are Layer 3 functions, not handled by switches.         |
| examining the destination MAC address to add new entries to the MAC address table  | ❌      | Switches add entries based on **source** MAC addresses.                |

---

### ✅ **Question 21**

**What is the purpose of the FCS field in a frame?**

| Option                                                            | Answer | Explanation                                             |
| ----------------------------------------------------------------- | ------ | ------------------------------------------------------- |
| to verify the logical address of the sending node                 | ❌      | Logical address verification is not FCS's purpose.      |
| to determine if errors occurred in the transmission and reception | ✅      | FCS holds the CRC for error checking.                   |
| to compute the CRC header for the data field                      | ❌      | FCS stores the result of a CRC, not compute it.         |
| to obtain the MAC address of the sending node                     | ❌      | The MAC address is in the frame header, not in the FCS. |

---

### ✅ **Question 22**

**A network administrator is connecting two modern switches using a straight-through cable. The switches are new and have never been configured. Which three statements are correct about the final result of the connection?**

| Option                                                                                               | Answer | Explanation                                                           |
| ---------------------------------------------------------------------------------------------------- | ------ | --------------------------------------------------------------------- |
| The auto-MDIX feature will configure the interfaces eliminating the need for a crossover cable.      | ✅      | Auto-MDIX automatically detects cable type.                           |
| The link between the switches will work at the fastest speed that is supported by both switches.     | ✅      | Auto-negotiation sets the best speed both switches support.           |
| The link between switches will work as full-duplex.                                                  | ✅      | Duplex mode is also auto-negotiated.                                  |
| The connection will not be possible unless the administrator changes the cable to a crossover cable. | ❌      | Auto-MDIX makes this unnecessary.                                     |
| The duplex capability has to be manually configured because it cannot be negotiated.                 | ❌      | Modern switches can auto-negotiate duplex.                            |
| If both switches support different speeds, they will each work at their own fastest speed.           | ❌      | They will work at the **highest common speed**, not different speeds. |

---

### ✅ **Question 23**

**Which switching method uses the CRC value in a frame?**

| Option            | Answer | Explanation                                                        |
| ----------------- | ------ | ------------------------------------------------------------------ |
| fragment-free     | ❌      | Fragment-free only checks the first 64 bytes.                      |
| fast-forward      | ❌      | Fast-forward starts forwarding before receiving the full frame.    |
| cut-through       | ❌      | Like fast-forward, doesn’t check CRC.                              |
| store-and-forward | ✅      | It receives the entire frame and checks the CRC before forwarding. |

---

### ✅ **Question 24**

**Which advantage does the store-and-forward switching method have compared with the cut-through switching method?**

| Option                                                | Answer | Explanation                                                                      |
| ----------------------------------------------------- | ------ | -------------------------------------------------------------------------------- |
| frame forwarding using IPv4 Layer 3 and 4 information | ❌      | Not specific to store-and-forward.                                               |
| collision detecting                                   | ❌      | Handled by media access methods like CSMA/CD.                                    |
| frame error checking                                  | ✅      | Store-and-forward checks the frame's integrity before forwarding.                |
| faster frame forwarding                               | ❌      | Cut-through is faster; store-and-forward is slower due to full-frame inspection. |

---

### ✅ **Question 25**

**A Layer 2 switch is used to switch incoming frames from a 1000BASE-T port to a port connected to a 100Base-T network. Which method of memory buffering would work best for this task?**

| Option                        | Answer | Explanation                                                             |
| ----------------------------- | ------ | ----------------------------------------------------------------------- |
| fixed configuration buffering | ❌      | Not a memory buffering method.                                          |
| port-based buffering          | ❌      | Each port uses its own memory; not efficient for speed mismatches.      |
| shared memory buffering       | ✅      | Allows frames from faster ports to be buffered and sent to slower ones. |
| level 1 cache buffering       | ❌      | Not a relevant buffering type in this context.                          |

---


Here are the answers for Questions 26, 27, 29, 32, 33, and 34 in the same **table format**:

---

### ✅ **Question 26**

**What are two examples of the cut-through switching method? (Choose two.)**

| Option                      | Answer | Explanation                                                                                          |
| --------------------------- | ------ | ---------------------------------------------------------------------------------------------------- |
| fragment-free switching     | ✅      | This is a type of cut-through switching that checks the first 64 bytes of a frame before forwarding. |
| QOS switching               | ❌      | Not a switching method; QoS is a network service feature.                                            |
| CRC switching               | ❌      | No such method; CRC is used in store-and-forward.                                                    |
| fast-forward switching      | ✅      | This is the purest form of cut-through; it begins forwarding before the full frame is received.      |
| store-and-forward switching | ❌      | This is a separate switching method that checks the entire frame including CRC.                      |

---

### ✅ **Question 27**

**What makes fiber preferable to copper cabling for interconnecting buildings? (Choose three.)**

| Option                            | Answer | Explanation                                                           |
| --------------------------------- | ------ | --------------------------------------------------------------------- |
| greater distances per cable run   | ✅      | Fiber supports much longer distances than copper without signal loss. |
| limited susceptibility to EMI/RFI | ✅      | Fiber is immune to electromagnetic and radio frequency interference.  |
| durable connections               | ❌      | Fiber is actually more fragile than copper.                           |
| lower installation cost           | ❌      | Fiber is usually more expensive to install.                           |
| greater bandwidth potential       | ✅      | Fiber supports much higher bandwidths than copper.                    |
| easily terminated                 | ❌      | Fiber termination is complex compared to copper.                      |

---

### ✅ **Question 29**

**What does the term "attenuation" mean in data communication?**

| Option                                            | Answer | Explanation                                             |
| ------------------------------------------------- | ------ | ------------------------------------------------------- |
| leakage of signals from one cable pair to another | ❌      | That's known as crosstalk.                              |
| loss of signal strength as distance increases     | ✅      | Attenuation is the weakening of a signal over distance. |
| time for a signal to reach its destination        | ❌      | That’s latency.                                         |
| strengthening of a signal by a networking device  | ❌      | That would be amplification or regeneration.            |

---

### ✅ **Question 32**

**What OSI physical layer term describes the amount of time, including delays, for data to travel from one point to another?**

| Option     | Answer | Explanation                                                        |
| ---------- | ------ | ------------------------------------------------------------------ |
| throughput | ❌      | Throughput is the actual data transferred per unit of time.        |
| latency    | ✅      | Latency is the delay or time it takes for a signal to travel.      |
| bandwidth  | ❌      | Bandwidth is the maximum capacity of a link.                       |
| goodput    | ❌      | Goodput is the actual useful data transferred, excluding overhead. |

---

### ✅ **Question 33**

**Which two functions are performed at the LLC sublayer of the OSI data link layer? (Choose two.)**

| Option                                                                 | Answer | Explanation                                                  |
| ---------------------------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Implements a trailer to detect transmission errors.                    | ❌      | This is handled by the MAC sublayer.                         |
| Adds Layer 2 control information to network protocol data.             | ✅      | LLC adds headers to identify network layer protocols.        |
| Provides synchronization between source and target nodes.              | ❌      | Not a core LLC function.                                     |
| Enables IPv4 and IPv6 to utilize the same network interface and media. | ✅      | LLC supports multiple network protocols over the same media. |
| Integrates various physical technologies.                              | ❌      | That is more related to MAC and Physical layers.             |

---

### ✅ **Question 34**

**What action will occur if a switch receives a frame with the destination MAC address FF\:FF\:FF\:FF\:FF\:FF?**

| Option                                                                                             | Answer | Explanation                                          |
| -------------------------------------------------------------------------------------------------- | ------ | ---------------------------------------------------- |
| The switch sends the frame to a connected router because the destination MAC address is not local. | ❌      | The address is broadcast, not destined for a router. |
| The switch does not forward the frame.                                                             | ❌      | Switches do forward broadcast frames.                |
| The switch forwards it out all ports except the ingress port.                                      | ✅      | This is standard behavior for broadcast frames.      |
| The switch shares the MAC address table entry with any connected switches.                         | ❌      | Switches do not share MAC address tables by default. |

---

Here is the answer to **Question 30** in the same **table format**:

---

### ✅ **Question 30**

**Refer to the exhibit. What is wrong with the displayed termination?**

| Option                                                  | Answer | Explanation                                                                                  |
| ------------------------------------------------------- | ------ | -------------------------------------------------------------------------------------------- |
| The woven copper braid should not have been removed.    | ❌      | This applies to coaxial cables, not twisted-pair Ethernet cables.                            |
| The wrong type of connector is being used.              | ❌      | No evidence suggests that the RJ45 connector is incorrect.                                   |
| The wires are too thick for the connector that is used. | ❌      | There's no indication of wire thickness being the issue.                                     |
| The untwisted length of each wire is too long.          | ✅      | Excessive untwisting increases crosstalk and signal interference, violating cable standards. |

---

Absolutely! Here's **Question 28** in the **same table format** as requested:

---

### ✅ **Question 28**

**Refer to the exhibit. The PC is connected to the console port of the switch. All the other connections are made through FastEthernet links. Which types of UTP cables can be used to connect the devices?**

| Connection                      | Cable Type       | Explanation                                                                                       |
| ------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------- |
| 1 - PC to Switch (Console Port) | Rollover         | Rollover cables are used to connect a PC's serial port to the console port of a switch or router. |
| 2 - Switch to Router            | Crossover        | A crossover cable is traditionally used between different device types (switch ↔ router).         |
| 3 - Router to Router            | Straight-through | When connecting routers through Ethernet interfaces, a straight-through cable can be used.        |

| Option                                            | Answer | Explanation                                                                    |
| ------------------------------------------------- | ------ | ------------------------------------------------------------------------------ |
| 1 - rollover, 2 - straight-through, 3 - crossover | ❌      | The Switch-Router connection requires a crossover, not straight-through.       |
| 1 - crossover, 2 - straight-through, 3 - rollover | ❌      | The PC-Switch Console connection must use a rollover cable, not a crossover.   |
| 1 - crossover, 2 - rollover, 3 - straight-through | ❌      | The Switch-Router link should not use a rollover cable.                        |
| 1 - rollover, 2 - crossover, 3 - straight-through | ✅      | This matches standard cabling practices for these types of device connections. |

---
Here is the **Question 3** formatted using the **matching table format**:

---

### ✅ **Question 3**

**Match the situation with the appropriate use of network media.**

| **Situation**                       | **Appropriate Use of Network Media** | **Explanation**                                                                 |
| ----------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------- |
| horizontal cabling structure        | **Copper cables**                    | Copper is commonly used for short-distance horizontal cabling within buildings. |
| desktop PCs in an enterprise office | **Copper cables**                    | Ideal for cost-effective wired connections at desks.                            |
| backbone cabling in an enterprise   | **Fiber-optic cables**               | Supports high bandwidth and long distances across floors or buildings.          |
| long-haul networks                  | **Fiber-optic cables**               | Preferred for high-speed data over long distances, like between cities.         |
| guest access in a coffee shop       | **Wireless**                         | Provides convenient, flexible access for multiple mobile users.                 |
| waiting rooms in a hospital         | **Wireless**                         | Eliminates physical cabling, providing safe and convenient access for patients. |

---

Let me know if you'd like this added to a document or want the next question formatted too!





Question 31
file_download
PT Activity

Open the PT Activity. Perform the tasks in the activity instructions and then answer the question.

Which port does Switch0 use to send frames to the host with the IPv4 address 10.1.1.5?


1)
Fa0/9

2)
Fa0/5

3)
Fa0/1

4)
Fa0/11
