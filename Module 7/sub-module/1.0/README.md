**Module: Ethernet Switching**
**Objective: Explain how Ethernet operates in a switched network**

---

### 📘 What Will You Learn in This Module?

You will learn **how Ethernet works in a switched environment**, including how switches use **MAC addresses** to forward data, how **Ethernet frames** are structured, and how switches handle **different speeds** and **forwarding methods**.

---

### 🔍 Topics and Their Meanings (with Examples)

| **Topic Title**                          | **Topic Objective**                                                                     | **Explanation with Example**                                                                                                                                                                                                                                                                                                                                                                             |
| ---------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Ethernet Frame**                       | Explain how the Ethernet sublayers are related to the frame fields.                     | An Ethernet frame is like an envelope for sending data. It includes parts like **source MAC, destination MAC, type, data, and CRC**. Example: If computer A wants to send data to computer B, it wraps the data in an Ethernet frame with B’s MAC address.                                                                                                                                               |
| **Ethernet MAC Address**                 | Describe the Ethernet MAC address.                                                      | A MAC (Media Access Control) address is a **unique hardware address** for each device’s network card. Example: `00:1A:2B:3C:4D:5E`. Think of it like a house address used to deliver packages.                                                                                                                                                                                                           |
| **The MAC Address Table**                | Explain how a switch builds its MAC address table and forwards frames.                  | A switch learns which devices are connected to which ports by reading source MAC addresses in the frames it receives. Example: If a frame from MAC `AA:BB:CC:DD:EE:01` arrives on port 1, the switch saves this info and later sends frames to this MAC only through port 1.                                                                                                                             |
| **Switch Speeds and Forwarding Methods** | Describe switch forwarding methods and port settings available on Layer 2 switch ports. | Switches can work at different speeds like **10 Mbps, 100 Mbps, 1 Gbps**. They use forwarding methods like: <br> - **Store-and-Forward**: waits for whole frame to arrive before sending (more accurate) <br> - **Cut-through**: starts forwarding after reading destination MAC (faster, less accurate). <br>Example: In a gaming café, fast cut-through switching may be preferred for quick response. |

---

Would you like a simple diagram of how a switch forwards frames using MAC addresses?
