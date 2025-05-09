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

### ✅ **7.1.3 MAC Sublayer – Simplified Explanation**

#### **What is the MAC Sublayer?**

The **MAC (Media Access Control) Sublayer** is responsible for:

* **Data Encapsulation**: Wrapping the data into Ethernet frames.
* **Accessing the Media**: Managing how devices access the network medium (cable or fiber).

---

### 📦 **Data Encapsulation – What’s Inside the Ethernet Frame?**

The **Ethernet Frame** has the following important parts:

1. **Ethernet Frame Structure**: This is the internal setup of how data is organized within the frame.
2. **Ethernet Addressing**:

   * **Source MAC address**: The sender’s address.
   * **Destination MAC address**: The recipient’s address.
     Example: If Computer A sends data to Computer B, the frame will have Computer A’s MAC as the source and Computer B’s MAC as the destination.
3. **Ethernet Error Detection**: The frame includes a **Frame Check Sequence (FCS)** that detects errors during transmission. If a collision or transmission error occurs, FCS helps identify the problem.

#### ⚙️ **Example:**

Imagine sending a letter to your friend:

* **Address** on the envelope (MAC addresses).
* **Letter content** (data).
* **Return address** (FCS for error detection).

---

### 🌐 **Accessing the Media – How Data is Sent**

Ethernet can run on various media like **copper cables** and **fiber optics**, as specified in the **IEEE 802.3** standard. Here’s how different standards work:

| **Standard**                           | **Description**             | **Media Type**        |
| -------------------------------------- | --------------------------- | --------------------- |
| **IEEE 802.3u (Fast Ethernet)**        | 100 Mbps Ethernet           | Copper (Twisted Pair) |
| **IEEE 802.3z (Gigabit Ethernet)**     | 1 Gbps Ethernet over Fiber  | Fiber-Optic           |
| **IEEE 802.3ab (Gigabit Ethernet)**    | 1 Gbps Ethernet over Copper | Copper (Twisted Pair) |
| **IEEE 802.3ae (10 Gigabit Ethernet)** | 10 Gbps Ethernet over Fiber | Fiber-Optic           |

#### ⚙️ **Example:**

* **Ethernet over copper (IEEE 802.3u)**: Think of **100 Mbps** Ethernet over a **twisted pair cable** (similar to a phone line).
* **Ethernet over fiber (IEEE 802.3z)**: **1 Gbps** Ethernet using **fiber-optic cables** (very fast and used for long distances).

---

### 🔄 **Access Control – How Devices Share the Network**

In older Ethernet systems using hubs (before switches), devices shared a **half-duplex** connection, meaning **only one device could transmit at a time**. This was managed by a protocol called **CSMA/CD** (Carrier Sense Multiple Access with Collision Detection).

* **CSMA/CD**: Devices **listen** to see if the network is free, then **transmit**. If two devices transmit simultaneously, a **collision** occurs, and they **back off** and retry.

#### ⚙️ **Example:**

Imagine a **walkie-talkie** system where only one person can talk at a time:

* **Listen**: Wait until the channel is clear.
* **Talk**: Transmit your message.
* **Collision**: If someone talks at the same time, you both stop and retry.

---

### 🖥 **Modern Ethernet with Switches – Full-Duplex**

Today’s Ethernet uses **switches** that allow **full-duplex communication**. This means **both devices can send and receive data simultaneously** without using CSMA/CD, which makes data transfer faster and more efficient.

---

### 📌 **Summary:**

* **MAC Sublayer**: Responsible for framing data and controlling how devices access the medium.
* **Ethernet Frame**: Includes MAC addresses and FCS for error checking.
* **Access Control**: Older systems used CSMA/CD, but modern Ethernet uses **full-duplex** with switches, eliminating the need for CSMA/CD.

### ✅ **7.1.4 Ethernet Frame Fields – Simplified Explanation**

#### **Ethernet Frame Structure**

An **Ethernet frame** is the structure used for data transmission over Ethernet networks. The frame consists of various fields, each playing a specific role. The **minimum Ethernet frame size** is **64 bytes**, and the **maximum** is **1518 bytes**.

---

### **Fields in the Ethernet Frame:**

1. **Preamble and Start Frame Delimiter (SFD)** - **8 bytes**

   * **Purpose**: Used for synchronization between the sending and receiving devices. This tells the receiving device to prepare for an incoming frame.
   * **Breakdown**:

     * **7 bytes** for **Preamble**: Synchronizes devices.
     * **1 byte** for **SFD**: Marks the start of the frame.

2. **Destination MAC Address** - **6 bytes**

   * **Purpose**: Identifies the recipient device.
   * **Details**: If the frame's destination MAC matches the device's MAC, it accepts the frame. It can be **unicast (one device)**, **multicast (multiple devices)**, or **broadcast (all devices)**.
   * **Example**: If the destination address is the MAC of Computer B, only Computer B accepts the frame.

3. **Source MAC Address** - **6 bytes**

   * **Purpose**: Identifies the sender (originating NIC or network interface).
   * **Example**: If Computer A sends a frame, Computer A's MAC is listed as the source.

4. **Type/Length** - **2 bytes**

   * **Purpose**: Specifies the upper-layer protocol being used in the frame (e.g., IPv4, IPv6, or ARP).
   * **Example**:

     * **0x800**: IPv4
     * **0x86DD**: IPv6
     * **0x806**: ARP

5. **Data** - **46 to 1500 bytes**

   * **Purpose**: This is the **payload** or the actual data being transferred, typically from a higher layer (e.g., an IPv4 packet).
   * **Minimum Size**: The Ethernet frame must be **at least 64 bytes** long, so if the data is smaller than 46 bytes, padding is added to meet the minimum size.

6. **Frame Check Sequence (FCS)** - **4 bytes**

   * **Purpose**: **Error detection**. The FCS field contains a **Cyclic Redundancy Check (CRC)** value, which is used to detect transmission errors.
   * **How it works**:

     * The sender generates a CRC based on the data and places it in the FCS.
     * The receiver also generates a CRC and compares it with the one in the FCS field.
     * If the two CRCs match, the frame is considered error-free. If not, the frame is discarded.

---

### 📦 **Ethernet Frame Summary**

| **Field**                      | **Length**        | **Purpose**                                                                             |
| ------------------------------ | ----------------- | --------------------------------------------------------------------------------------- |
| **Preamble & SFD**             | **8 bytes**       | Synchronization; tells devices to get ready to receive a frame.                         |
| **Destination MAC Address**    | **6 bytes**       | Identifies the recipient of the frame.                                                  |
| **Source MAC Address**         | **6 bytes**       | Identifies the sender of the frame.                                                     |
| **Type/Length**                | **2 bytes**       | Specifies the protocol (e.g., IPv4, IPv6, ARP) of the encapsulated data.                |
| **Data**                       | **46-1500 bytes** | Contains the actual data being transmitted. If smaller than 46 bytes, padding is added. |
| **FCS (Frame Check Sequence)** | **4 bytes**       | Error detection using CRC. If the CRC doesn't match, the frame is discarded.            |

---

### ⚠️ **Special Frame Sizes:**

* **Runt Frame**: A frame smaller than 64 bytes. It is considered **invalid** and discarded by the receiving device.
* **Jumbo Frame**: A frame larger than 1500 bytes. It’s typically used in **Gigabit Ethernet** or **Fast Ethernet** networks, supporting higher data volumes. Not all devices support jumbo frames.

---

### **Example:**

* If Computer A sends a message to Computer B:

  * **Destination MAC**: Computer B’s MAC.
  * **Source MAC**: Computer A’s MAC.
  * **Data**: The actual message.
  * **FCS**: Ensures no errors during transmission.

Would you like further clarification or an example related to error detection (FCS)?

