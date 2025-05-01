# Peer-to-Peer (P2P) Networking

## 🔍 What is Peer-to-Peer Networking?

A **Peer-to-Peer (P2P)** network is a type of computer network where all devices (called "peers") are connected directly. Each device can act as both a **client** and a **server**, meaning they can both request and provide services.

---

## 🖥️ Simple Example

Imagine a small home or office network:

- **Computer A** is connected to a **printer** and shares it.
- **Computer B** shares **files**.
- Both are connected through a simple network (like Wi-Fi or LAN).

Now, **Computer A** can print documents and also get files from **Computer B**, and vice versa. No central server is needed.

---

## ✅ Advantages of P2P Networking

- Easy to set up
- Less complex to manage
- Lower cost (no need for dedicated servers or expensive hardware)
- Ideal for small tasks like:
  - File sharing
  - Printer sharing

---

## ❌ Disadvantages of P2P Networking

- No centralized control or administration
- Less secure
- Not scalable for large networks
- Slower performance (since each device does multiple tasks)

---

## 📌 Use Case

Best suited for **small offices** or **home networks** where users need basic file or printer sharing without complex setup.

<img src="Module 1/network.jpg" alt="Module 1 Image" width="300"/>





🖧 Intermediary Network Devices
| Device Name        | Role / Function                                                                 | Example (What it Does)                                                                 |
|--------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Repeater**        | Regenerates and retransmits weak signals to extend the distance of the network | Boosts a weak signal across long cables to maintain a strong connection                 |
| **Hub (Ethernet Hub)** | Multiport repeater; sends data to all connected devices                      | Shares internet to all PCs in a small office, even if not needed                        |
| **Switch**          | Connects devices in a LAN and forwards data only to the intended device        | Sends files from one computer to another without flooding the whole network             |
| **Router**          | Connects multiple networks and decides best path for data                      | Connects your home Wi-Fi to the internet and routes data to correct devices             |
| **Bridge**          | Connects and filters traffic between two network segments                      | Joins two LANs and controls traffic to reduce congestion                                |
| **Modem**           | Converts digital data to analog and vice versa (used for internet access)      | Lets your computer talk to the internet via telephone or cable line                     |
| **Access Point (AP)** | Allows wireless devices to connect to a wired network                         | Connects your mobile phone to Wi-Fi in a college or cafe                                |
| **Firewall**        | Controls what data is allowed in or out based on security rules                | Blocks suspicious websites or hackers from entering your network                        |
| **Gateway**         | Acts as a translator between different network protocols                       | Allows communication between different types of networks (e.g., LAN to cloud service)   |
| **Load Balancer**   | Distributes network traffic across multiple servers                            | Helps a website handle many visitors without crashing                                   |



1.2.5 Network Media
| **Media Type** | **Description** | **Common Cable Types / Technologies** | **Key Features** | **Example Use Cases** |
|----------------|-----------------|---------------------------------------|------------------|-----------------------|
| **Copper Cables** | Data is transmitted as electrical signals through metal wires. | UTP / STP / Coaxial / Cat5e / Cat6 / Cat6a / Cat7 / Cat8 | Cheaper, easy to install, suitable for short distances. | Ethernet LANs, telephone lines, CCTV systems. |
| **Fiber Optic Cables** | Data is transmitted as light pulses through glass or plastic fibers. | Single-mode (OS1 / OS2) / Multi-mode (OM1 / OM2 / OM3 / OM4 / OM5) | Very fast, supports long distances, immune to electromagnetic interference. | High-speed internet backbones, data centers, long-distance telecommunications. |
| **Wireless** | Data is transmitted through the air using electromagnetic waves. | Wi-Fi / Bluetooth / Infrared / Radio Waves / Microwaves / Satellite | No physical cables needed, flexible, but can have signal issues. | Mobile networks, Wi-Fi hotspots, satellite communications, remote controls. |

Note:

UTP: Unshielded Twisted Pair

STP: Shielded Twisted Pair

Cat5e/Cat6/etc.: Categories of Ethernet cables with varying performance characteristics.

Single-mode Fiber: Suitable for long-distance communication.

Multi-mode Fiber: Suitable for shorter distances with high data rates.



## 1.2.6 quize
## 📝 Quiz: Networking Basics

### **Question 1**
**Which of the following is the name for all computers connected to a network that participate directly in network communication?**

- [ ] Servers  
- [ ] Intermediary devices  
- [x] Hosts  
- [ ] Media  

**✅ Correct Answer:** Hosts  
**Explanation:** Hosts are all computers connected to a network that participate directly in network communication. :contentReference[oaicite:0]{index=0}&#8203;:contentReference[oaicite:1]{index=1}

---

### **Question 2**
**When data is encoded as pulses of light, which media is being used to transmit the data?**

- [ ] Wireless  
- [x] Fiber-optic cable  
- [ ] Copper cable  

**✅ Correct Answer:** Fiber-optic cable  
**Explanation:** :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}&#8203;:contentReference[oaicite:4]{index=4}

---

### **Question 3**
**Which two devices are intermediary devices? (Choose two)**

- [ ] Hosts  
- [x] Routers  
- [ ] Servers  
- [x] Switches  

**✅ Correct Answers:** Routers and Switches  
**Explanation:** :contentReference[oaicite:5]{index=5} :contentReference[oaicite:6]{index=6}&#8203;:contentReference[oaicite:7]{index=7}

---






### 📘 Network Devices Overview
```
🖥️ End Devices
End devices are user-operated hardware that serve as the source or destination of data within a network.​

Desktop Computer

Laptop

Printer

IP Phone

Wireless Tablet

TelePresence Endpoint

🔁 Intermediary Devices
Intermediary devices facilitate the flow of data across the network by directing and managing traffic.​

Wireless Router

LAN Switch

Router

Multilayer Switch

Firewall Appliance

🌐 Network Media
Network media are the physical or wireless channels through which data travels from one device to another.​

Wireless Media

LAN Media

WAN Media
```





### Network Representations
```
Here’s a concise summary with examples:

Network Interface Card (NIC):
A hardware component in a device that allows it to connect to a network.
🔹 Example: A laptop’s Wi-Fi card or Ethernet port is a NIC.

Physical Port:
A tangible connector on a device where network cables plug in.
🔹 Example: The RJ-45 Ethernet jack on a switch or PC.

Interface:
A logical or specialized port used to connect networks, especially on routers.
🔹 Example: A router’s GigabitEthernet0/0 interface connects to the internet or another LAN.
```



# 📘 Check Your Understanding – Network Representations and Topologies

```
Network Interface Card (NIC):
A hardware component in a device that allows it to connect to a network.
🔹 Example: A laptop’s Wi-Fi card or Ethernet port is a NIC.

Physical Port:
A tangible connector on a device where network cables plug in.
🔹 Example: The RJ-45 Ethernet jack on a switch or PC.

Interface:
A logical or specialized port used to connect networks, especially on routers.
🔹 Example: A router’s GigabitEthernet0/0 interface connects to the internet or another LAN.
```





### ✅ Question 1  
**Which connection physically connects the end device to the network?**

| Option | Answer | Explanation |
|--------|--------|-------------|
| 🅐 Port | ❌ Incorrect | A port is a physical outlet, but by itself, it does not connect the device — it’s where the connection is made. |
| 🅑 NIC (Network Interface Card) | ✅ Correct | A NIC is the hardware inside the end device that connects it to a network via cables (Ethernet) or wirelessly (Wi-Fi).<br>🔹 *Example:* Ethernet or Wi-Fi card in a laptop or desktop.<br>🔹 *Use:* Required for devices to send/receive data over a network. |
| 🅒 Interface | ❌ Incorrect | Interfaces are used on networking devices like routers to connect networks, not end devices. |

---

### ✅ Question 2  
**Which connections are specialized ports on a networking device that connect to individual networks?**

| Option | Answer | Explanation |
|--------|--------|-------------|
| 🅐 Port | ❌ Incorrect | Generic term for a physical connector. Not all ports are designed to connect to networks. |
| 🅑 NIC | ❌ Incorrect | A NIC is for end devices, not networking devices like routers or switches. |
| 🅒 Interface | ✅ Correct | An interface is a specialized port on routers/switches used to connect to different networks.<br>🔹 *Example:* `GigabitEthernet0/1` on a Cisco router.<br>🔹 *Use:* Connects to LANs, WANs, or the internet. |

---

### ✅ Question 3  
**Which type of network topology lets you see which end devices are connected to which intermediary devices and what media is being used?**

| Option | Answer | Explanation |
|--------|--------|-------------|
| 🅐 Physical topology | ✅ Correct | Shows the actual layout of devices and cables in a network.<br>🔹 *Example:* Diagram showing a PC connected to a switch via Ethernet.<br>🔹 *Use:* For planning, installation, and troubleshooting. |
| 🅑 Logical topology | ❌ Incorrect | Shows how data flows through the network, not the physical layout. |

---

### ✅ Question 4  
**Which type of network topology lets you see the actual location of intermediary devices and cable installation?**

| Option | Answer | Explanation |
|--------|--------|-------------|
| 🅐 Physical topology | ✅ Correct | It shows the physical layout of cables, devices, and locations.<br>🔹 *Example:* Floor plan with exact router/switch placement and cable paths.<br>🔹 *Use:* Network cabling, hardware installation. |
| 🅑 Logical topology | ❌ Incorrect | It doesn’t show physical placement, only logical flow (like IP addressing and routing paths). |

---

### 📝 Summary Table

| Question | Correct Answer     | Explanation |
|----------|--------------------|-------------|
| 1        | NIC                | NIC physically connects a device to the network. |
| 2        | Interface          | Interfaces are specialized router/switch ports that connect to networks. |
| 3        | Physical topology  | Shows which devices are connected and what media (e.g., Ethernet) is used. |
| 4        | Physical topology  | Shows actual physical layout and cable installation. |

