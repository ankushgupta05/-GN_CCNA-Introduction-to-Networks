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

Would you like the answers for Question 3 or any other questions you skipped?
