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

Here’s a **simple explanation** of **Ethernet Encapsulation** and **Data Link Sublayers** with **examples**:

---

### ✅ **7.1.1 Ethernet Encapsulation – Simplified**

#### 🔹 What is Ethernet?

Ethernet is a **wired LAN (Local Area Network)** technology used to connect devices like computers, switches, and routers using cables such as:

* Twisted pair (e.g., Cat5/Cat6)
* Fiber-optic
* Coaxial

#### 🔹 Where does Ethernet work?

Ethernet operates in the **Data Link Layer (Layer 2)** and **Physical Layer (Layer 1)** of the OSI model.

#### 🔹 Ethernet Speed Examples:

| **Speed** | **Meaning**                     |
| --------- | ------------------------------- |
| 10 Mbps   | Early Ethernet (slowest)        |
| 100 Mbps  | Fast Ethernet                   |
| 1 Gbps    | Gigabit Ethernet (common today) |
| 10 Gbps+  | Used in modern data centers     |

#### ⚙️ Example:

You connect your laptop to a router using a LAN cable. Ethernet handles the data from your laptop to the router using its rules (frame structure, addressing, and speed).

---

### ✅ **7.1.2 Data Link Sublayers – Simplified**

The **Data Link Layer** in Ethernet has two sublayers:

| **Sublayer**                   | **Function**                                                                                       | **Example**                                                                |
| ------------------------------ | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| **LLC (Logical Link Control)** | Communicates with higher layers (like IP), tells which network protocol (e.g., IPv4/IPv6) is used. | Think of it as a label telling whether data is for IPv4 or IPv6.           |
| **MAC (Media Access Control)** | Deals with hardware: adds MAC address, prepares data for transmission, controls access to media.   | Like writing the recipient’s MAC address on an envelope before sending it. |

#### ⚙️ Example:

When your laptop sends data to a printer:

* **LLC** says: “This is IPv4 data.”
* **MAC** says: “Send this to printer’s MAC address using Ethernet rules.”

---

### 📌 Summary with Visual:

```
[Network Layer - IPv4 or IPv6]
            ↓
[LLC - Says it's IPv4/IPv6]
            ↓
[MAC - Adds MAC addresses + prepares frame]
            ↓
[Physical Layer - Sends data over cable]
```

Would you like a diagram to visualize how LLC and MAC sublayers work together?
