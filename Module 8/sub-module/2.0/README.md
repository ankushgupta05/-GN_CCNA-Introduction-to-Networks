Here's a summarized explanation of the **IPv4 Packet Header** based on your provided text, organized in a clear and structured table format:

---

### **IPv4 Packet Header Fields**

| **Field**                        | **Size (bits)** | **Description**                                                                                                                             |
| -------------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Version**                      | 4               | Indicates the IP version. For IPv4, this is always set to `0100`.                                                                           |
| **Differentiated Services (DS)** | 8               | Used for packet priority and quality of service. <br> - First 6 bits: **DSCP** <br> - Last 2 bits: **ECN**                                  |
| **Time to Live (TTL)**           | 8               | Limits packet's lifetime. Decrements by 1 at each router. If it reaches 0, the packet is discarded and an ICMP error is sent to the sender. |
| **Protocol**                     | 8               | Identifies the next-layer protocol:<br> - ICMP (1), TCP (6), UDP (17), etc.                                                                 |
| **Header Checksum**              | 16              | Used to detect errors in the IPv4 header. Recalculated at each hop due to TTL decrement.                                                    |
| **Source IPv4 Address**          | 32              | IP address of the sender. Always a **unicast** address.                                                                                     |
| **Destination IPv4 Address**     | 32              | IP address of the receiver. Can be **unicast**, **multicast**, or **broadcast**.                                                            |
| **Internet Header Length (IHL)** | 4               | Specifies the header length in 32-bit words. Used to determine where the data starts.                                                       |
| **Total Length**                 | 16              | Total length of the IP packet (header + data).                                                                                              |
| **Identification**               | 16              | Helps identify fragments of the same original packet.                                                                                       |
| **Flags**                        | 3               | Controls fragmentation. For example, the "Don't Fragment (DF)" and "More Fragments (MF)" flags.                                             |
| **Fragment Offset**              | 13              | Used to reassemble fragmented packets in the correct order.                                                                                 |
| **Options and Padding**          | Variable        | Rarely used. Extra features, if needed. Padding ensures the header is a multiple of 32 bits.                                                |

---

### **Key Notes**

* **Source/Destination Addresses**: Most referenced; these usually stay the same throughout the packet’s journey.
* **TTL and Header Checksum**: Changed at each router.
* **Fragmentation**: Handled using Identification, Flags, and Fragment Offset.
* **Options**: Advanced usage, not commonly applied.

Would you like a diagram or visual to go along with this explanation?
