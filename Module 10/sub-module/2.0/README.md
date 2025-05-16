Here’s a **clear and structured summary** of section **10.2.1 – Configure Router Interfaces**, including explanation, commands, and key notes.

---

## 🔧 10.2.1 Configure Router Interfaces

Once basic settings are configured on a router, the **next critical step** is to **configure the router interfaces**. Without interface configuration, routers cannot communicate with other devices on the network.

---

### 🖥️ Example Router Model

Cisco **ISR 4321** router includes:

* **G0/0/0** – GigabitEthernet 0/0/0
* **G0/0/1** – GigabitEthernet 0/0/1

---

### 🛠️ General Interface Configuration Steps

```plaintext
Router(config)# interface type-and-number
Router(config-if)# description description-text
Router(config-if)# ip address ipv4-address subnet-mask
Router(config-if)# ipv6 address ipv6-address/prefix-length
Router(config-if)# no shutdown
```

#### ✅ Explanation of Each Command:

| Command                                 | Purpose                                                      |
| --------------------------------------- | ------------------------------------------------------------ |
| `interface G0/0/0`                      | Enters interface configuration mode for a specific interface |
| `description Link to XYZ`               | Adds a description (for documentation and troubleshooting)   |
| `ip address 192.168.10.1 255.255.255.0` | Assigns an IPv4 address and subnet mask                      |
| `ipv6 address 2001:db8:acad:10::1/64`   | Assigns an IPv6 address                                      |
| `no shutdown`                           | Activates the interface (required for it to function)        |

---

### 📝 Important Notes:

* **`description`** is optional but recommended for **network clarity and troubleshooting**.
* **`no shutdown`** is **required** to activate the interface (interfaces are **shut down by default**).
* The interface must be **physically connected** to another device (e.g., router or switch) for the link to become **fully active**.
* On **router-to-router** links (no switch in between), **both sides** of the connection must be configured and enabled.

---

### 📢 Interface Status Message

When an interface is successfully brought up with `no shutdown`, you should see messages like:

```plaintext
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0/0, changed state to up
```

> ✅ These messages confirm that both the **physical** and **data link** layers are operational.

---

Here's a clean breakdown of **Section 10.2.2 – Configure Router Interfaces Example**, using the provided scenario with a **topology explanation**, **command summary**, and **expected output**.

---

## 🔧 10.2.2 Configure Router Interfaces – Example

### 🖥️ Network Topology Summary (Left to Right)

```
[PC1] -- [Switch] -- G0/0/0 [R1] G0/0/1 -- [R2] -- [Switch] -- [PC2] -- Internet
```

### 🧠 IP Addressing:

| Device/Interface | IPv4 Address    | IPv6 Address           | Network/Subnet                 |
| ---------------- | --------------- | ---------------------- | ------------------------------ |
| PC1              | 192.168.10.10   | 2001\:db8\:acad:10::10 | 192.168.10.0/24 / acad:10::/64 |
| R1 G0/0/0        | 192.168.10.1    | 2001\:db8\:acad:10::1  | LAN side                       |
| R1 G0/0/1        | 209.165.200.225 | 2001\:db8\:feed:224::1 | R1–R2 WAN                      |
| R2 G0/0/1        | 209.165.200.226 | 2001\:db8\:feed:224::2 | R1–R2 WAN                      |
| R2 LAN (to PC2)  | 10.1.1.1        | 2001\:db8\:cafe:1::1   | 10.1.1.0/24 / cafe:1::/64      |
| PC2              | 10.1.1.10       | 2001\:db8\:cafe:1::10  | R2 LAN                         |

---

## 🛠️ Configuration on **R1**

### 🔹 Step-by-step Commands:

#### 🔸 G0/0/0 (LAN – toward PC1)

```bash
R1> enable
R1# configure terminal
R1(config)# interface gigabitEthernet 0/0/0
R1(config-if)# description Link to LAN
R1(config-if)# ip address 192.168.10.1 255.255.255.0
R1(config-if)# ipv6 address 2001:db8:acad:10::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
```

✅ **Expected Output**:

```plaintext
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/0, changed state to down
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0/0, changed state to up
```

---

#### 🔸 G0/0/1 (WAN – toward R2)

```bash
R1(config)# interface gigabitEthernet 0/0/1
R1(config-if)# description Link to R2
R1(config-if)# ip address 209.165.200.225 255.255.255.252
R1(config-if)# ipv6 address 2001:db8:feed:224::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
```

✅ **Expected Output**:

```plaintext
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/1, changed state to down
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/1, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0/1, changed state to up
```

---

### 📌 Summary

| Interface | Description | IPv4 Address       | IPv6 Address              |
| --------- | ----------- | ------------------ | ------------------------- |
| G0/0/0    | Link to LAN | 192.168.10.1/24    | 2001\:db8\:acad:10::1/64  |
| G0/0/1    | Link to R2  | 209.165.200.225/30 | 2001\:db8\:feed:224::1/64 |

> ✅ These configurations enable R1 to communicate with both the **LAN (PC1)** and the **next router (R2)** over IPv4 and IPv6.

Let me know if you want the **R2 configuration example** or a **diagram** of this topology.
