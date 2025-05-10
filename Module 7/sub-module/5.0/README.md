Below are the Module Quiz questions formatted as requested.

---

### Question 1

Which two characteristics describe Ethernet technology? (Choose two.)

|                                            Option                                           |    Answer   | Explanation                                                    |
| :-----------------------------------------------------------------------------------------: | :---------: | :------------------------------------------------------------- |
|                         🅐 It is supported by IEEE 802.3 standards.                         |  ✅ Correct  | IEEE 802.3 defines Ethernet specifications.                    |
|                         🅑 It is supported by IEEE 802.5 standards.                         | ❌ Incorrect | IEEE 802.5 covers Token Ring, not Ethernet.                    |
|             🅒 It typically uses an average of 16 Mbps for data transfer rates.             | ❌ Incorrect | Ethernet speeds range from 10 Mbps to multi‐Gbps, not 16 Mbps. |
| 🅓 It uses unique MAC addresses to ensure that data is sent to the appropriate destination. |  ✅ Correct  | Ethernet uses 48-bit MACs to identify NICs on a LAN.           |
|                                 🅔 It uses a ring topology.                                 | ❌ Incorrect | Ethernet uses bus or star topologies, not ring.                |

---

### Question 2

What statement describes a characteristic of MAC addresses?

|                         Option                        |    Answer   | Explanation                                                |
| :---------------------------------------------------: | :---------: | :--------------------------------------------------------- |
|            🅐 They must be globally unique.           |  ✅ Correct  | MAC OUIs and NIC values are assigned to ensure uniqueness. |
| 🅑 They are only routable within the private network. | ❌ Incorrect | MACs are not routable at all; IP is used for routing.      |
|      🅒 They are added as part of a Layer 3 PDU.      | ❌ Incorrect | MACs are part of the Layer 2 frame header, not Layer 3.    |
|          🅓 They have a 32-bit binary value.          | ❌ Incorrect | MACs are 48-bit addresses.                                 |

---

### Question 3

What is the special value assigned to the first 24 bits of a multicast MAC address transporting an IPv4 packet?

|    Option   |    Answer   | Explanation                                                |
| :---------: | :---------: | :--------------------------------------------------------- |
| 🅐 01-5E-00 | ❌ Incorrect | Byte order is wrong; the IANA-reserved prefix is 01-00-5E. |
| 🅑 FF-00-5E | ❌ Incorrect | FF-FF-FF-FF-FF-FF is broadcast, not IPv4 multicast.        |
| 🅒 FF-FF-FF | ❌ Incorrect | That's the 48-bit broadcast MAC (all ones).                |
| 🅓 01-00-5E |  ✅ Correct  | IANA reserved prefix for IPv4 multicast (01-00-5E).        |

---

### Question 4

What will a host on an Ethernet network do if it receives a frame with a unicast destination MAC address that does not match its own MAC address?

|                                     Option                                    |    Answer   | Explanation                                                                           |
| :---------------------------------------------------------------------------: | :---------: | :------------------------------------------------------------------------------------ |
|                         🅐 It will discard the frame.                         |  ✅ Correct  | Hosts ignore frames not addressed to their MAC.                                       |
|                 🅑 It will forward the frame to the next host.                | ❌ Incorrect | Only switches forward; end hosts do not forward Ethernet frames.                      |
|                  🅒 It will remove the frame from the media.                  | ❌ Incorrect | “Removing” isn’t a valid host action—unused frames are just ignored.                  |
| 🅓 It will strip off the data-link frame to check the destination IP address. | ❌ Incorrect | Hosts only process IP if the MAC matches their own or is a valid broadcast/multicast. |

---

### Question 5

Which network device makes forwarding decisions based on the destination MAC address that is contained in the frame?

|    Option   |    Answer   | Explanation                                                    |
| :---------: | :---------: | :------------------------------------------------------------- |
| 🅐 Repeater | ❌ Incorrect | Repeaters simply amplify signals, no MAC-based decisions.      |
|    🅑 Hub   | ❌ Incorrect | Hubs broadcast to all ports; no MAC filtering.                 |
|  🅒 Switch  |  ✅ Correct  | Switches use MAC tables to forward frames to the correct port. |
|  🅓 Router  | ❌ Incorrect | Routers operate at Layer 3 (IP), not Layer 2.                  |

---

### Question 6

Which network device has the primary function to send data to a specific destination based on the information found in the MAC address table?

|   Option  |    Answer   | Explanation                                                      |
| :-------: | :---------: | :--------------------------------------------------------------- |
|   🅐 Hub  | ❌ Incorrect | Hubs do not maintain MAC tables.                                 |
| 🅑 Router | ❌ Incorrect | Routers use IP routing tables, not MAC tables.                   |
| 🅒 Switch |  ✅ Correct  | Switches maintain MAC-to-port mappings for forwarding.           |
|  🅓 Modem | ❌ Incorrect | Modems convert between digital and analog signals, no MAC logic. |

---

### Question 7

Which function or operation is performed by the LLC sublayer?

|                                  Option                                 |    Answer   | Explanation                                             |
| :---------------------------------------------------------------------: | :---------: | :------------------------------------------------------ |
|                    🅐 It performs data encapsulation.                   | ❌ Incorrect | That’s the role of the MAC and physical sublayers.      |
|              🅑 It communicates with upper protocol layers.             |  ✅ Correct  | LLC provides the interface between Layer 2 and Layer 3. |
|              🅒 It is responsible for media access control.             | ❌ Incorrect | That’s the MAC sublayer’s job.                          |
| 🅓 It adds a header and trailer to a packet to form an OSI Layer 2 PDU. | ❌ Incorrect | The MAC sublayer adds headers/trailers, not LLC.        |

---

### Question 8

What happens to runt frames received by a Cisco Ethernet switch?

|                                Option                               |    Answer   | Explanation                                                    |
| :-----------------------------------------------------------------: | :---------: | :------------------------------------------------------------- |
|                       🅐 The frame is dropped.                      |  ✅ Correct  | Frames smaller than the minimum size (64 bytes) are discarded. |
|     🅑 The frame is returned to the originating network device.     | ❌ Incorrect | Switches never “return” runt frames.                           |
| 🅒 The frame is broadcast to all other devices on the same network. | ❌ Incorrect | Discarded frames are not forwarded or broadcast.               |
|             🅓 The frame is sent to the default gateway.            | ❌ Incorrect | Switches don’t send runt frames to routers.                    |

---

### Question 9

What addressing information is recorded by a switch to build its MAC address table?

|                         Option                         |    Answer   | Explanation                                             |
| :----------------------------------------------------: | :---------: | :------------------------------------------------------ |
| 🅐 The destination Layer 3 address of incoming packets | ❌ Incorrect | Switches record MAC, not IP, information.               |
|  🅑 The destination Layer 2 address of outgoing frames | ❌ Incorrect | Switches learn from source addresses, not destinations. |
|    🅒 The source Layer 3 address of outgoing packets   | ❌ Incorrect | Layer 3 addresses are irrelevant to MAC tables.         |
|    🅓 The source Layer 2 address of incoming frames    |  ✅ Correct  | Switches map source MAC → incoming port for forwarding. |

---

### Question 10

What is auto-MDIX?

|                          Option                          |    Answer   | Explanation                                        |
| :------------------------------------------------------: | :---------: | :------------------------------------------------- |
|                 🅐 A type of Cisco switch                | ❌ Incorrect | It’s a feature, not a switch model.                |
|               🅑 An Ethernet connector type              | ❌ Incorrect | RJ-45 is the connector; auto-MDIX is a feature.    |
| 🅒 A feature to automatically determine speed and duplex | ❌ Incorrect | That’s autonegotiation.                            |
|       🅓 A feature that detects Ethernet cable type      |  ✅ Correct  | Auto-MDIX swaps MDI/MDIX pairs so any cable works. |

---

### Question 11

What type of address is 01-00-5E-0A-00-02?

|                            Option                           |    Answer   | Explanation                                            |
| :---------------------------------------------------------: | :---------: | :----------------------------------------------------- |
| 🅐 An address that reaches every host inside a local subnet | ❌ Incorrect | That’s the broadcast MAC (FF-FF-FF-FF-FF-FF).          |
|         🅑 An address that reaches one specific host        | ❌ Incorrect | Unicast MACs target one NIC; multicast targets groups. |
|     🅒 An address that reaches every host in the network    | ❌ Incorrect | That’s still broadcast.                                |
|     🅓 An address that reaches a specific group of hosts    |  ✅ Correct  | 01-00-5E prefix indicates an IPv4 multicast group.     |

---

### Question 12

Which statement is true about MAC addresses?

|                             Option                            |    Answer   | Explanation                                        |
| :-----------------------------------------------------------: | :---------: | :------------------------------------------------- |
|         🅐 MAC addresses are implemented by software.         | ❌ Incorrect | MACs are burned into NIC hardware (firmware).      |
|    🅑 A NIC only needs a MAC address if connected to a WAN.   | ❌ Incorrect | MACs are required on every Ethernet LAN interface. |
| 🅒 The first three bytes are used by the vendor assigned OUI. |  ✅ Correct  | OUI identifies the NIC manufacturer.               |
|    🅓 The ISO is responsible for MAC addresses regulations.   | ❌ Incorrect | IEEE (not ISO) oversees MAC standards.             |

---

### Question 13

What are the two sizes (minimum and expected maximum) of an Ethernet frame? (Choose two.)

|     Option    |    Answer   | Explanation                                                       |
| :-----------: | :---------: | :---------------------------------------------------------------- |
|  🅐 56 bytes  | ❌ Incorrect | Minimum Ethernet frame size is 64 bytes (including header & CRC). |
|  🅑 64 bytes  |  ✅ Correct  | Smallest valid Ethernet frame is 64 bytes.                        |
|  🅒 128 bytes | ❌ Incorrect | Maximum standard frame size is larger than 128 bytes.             |
| 🅓 1024 bytes | ❌ Incorrect | Jumbo frames can exceed this, but standard max is 1518 bytes.     |
| 🅔 1518 bytes |  ✅ Correct  | Typical maximum Ethernet frame size without VLAN tags.            |

---

### Question 14

Which two functions or operations are performed by the MAC sublayer? (Choose two.)

|                             Option                             |    Answer   | Explanation                                                   |
| :------------------------------------------------------------: | :---------: | :------------------------------------------------------------ |
|         🅐 It is responsible for Media Access Control.         |  ✅ Correct  | MAC sublayer arbitrates access to the shared medium.          |
|       🅑 It performs the function of NIC driver software.      | ❌ Incorrect | NIC drivers are OS/software components, not the MAC sublayer. |
|   🅒 It adds a header and trailer to form an OSI Layer 2 PDU.  |  ✅ Correct  | MAC appends frame header/trailer around LLC data.             |
|   🅓 It handles communication between upper and lower layers.  | ❌ Incorrect | That’s the LLC (upper) and physical (lower) sublayers’ roles. |
| 🅔 It adds control information to network protocol layer data. | ❌ Incorrect | Control info at Layer 2 is MAC header/trailer, covered above. |

---

Let me know if you’d like any further formatting or review!
