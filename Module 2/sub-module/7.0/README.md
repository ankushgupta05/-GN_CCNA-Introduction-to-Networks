Here is the content added in a clear and organized way for your `README.md` file:

---

## 💻 2.7.3 Syntax Checker – Verify Windows PC IP Configuration

To **check IP settings** on a Windows PC, you can use the **Command Prompt**.

### ✅ Command:

```bash
ipconfig
```

### 📄 Sample Output:

```
C:\>ipconfig

Windows IP Configuration

Ethernet adapter Local Area Connection:

   Connection-specific DNS Suffix  . : cisco.com
   Link-local IPv6 Address . . . . . : fe80::b0ef:ca42:af2c:c6c7%16
   IPv4 Address. . . . . . . . . . . : 192.168.1.10
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1
```

This output confirms the IPv4 address, subnet mask, and default gateway assigned to the PC—either manually or via DHCP.

---
Here's the explanation written in clear markdown format for your `README.md` file:

---




## 🔧 2.7.4 Switch Virtual Interface (SVI) Configuration

To allow **remote management of a switch**, an **IP address must be assigned to a Switch Virtual Interface (SVI)**. An SVI does not refer to a physical port but a **virtual interface**, typically `VLAN 1`.

### 📘 Steps to Configure SVI on a Switch:

1. Enter global configuration mode.
2. Enter VLAN 1 interface configuration.
3. Assign an IPv4 address and subnet mask.
4. Enable the interface using `no shutdown`.
5. (Optional but common) Set the **default gateway** for remote communication.

### ✅ Example Configuration:

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# interface vlan 1
Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0
Sw-Floor-1(config-if)# no shutdown
Sw-Floor-1(config-if)# exit
Sw-Floor-1(config)# ip default-gateway 192.168.1.1
```

### 💡 Notes:

* `interface vlan 1` creates a virtual interface.
* `ip address` assigns the IPv4 address to the SVI.
* `no shutdown` activates the interface.
* `ip default-gateway` sets the path for the switch to communicate outside its subnet (i.e., to a router).

This setup allows the switch to be managed over the network just like any other IP-enabled device.

---

Here’s how you can write section **2.7.5** in your `README.md` file using a clear and structured format:

---

## ⚙️ 2.7.5 Syntax Checker - Configure a Switch Virtual Interface

This section demonstrates how to configure a **Switch Virtual Interface (SVI)** on VLAN 1 to enable network communication and remote management.

### 🛠️ Step-by-Step Configuration:

1. **Enter interface configuration mode for VLAN 1**:

   ```bash
   Switch(config)#interface vlan 1
   ```

2. **Configure the IPv4 address and subnet mask**:

   ```bash
   Switch(config-if)#ip address 192.168.1.20 255.255.255.0
   ```

3. **Enable the interface**:

   ```bash
   Switch(config-if)#no shutdown
   %LINK-5-CHANGED: Interface Vlan1, changed state to up
   ```

### ✅ Result:

You have successfully configured the switch virtual interface for **VLAN 1**. This allows the switch to participate in the network and be accessed remotely for management.

---






Great! Below is the updated `README.md` content **with exact commands** and **where they are fired from**, clearly marked for **Switch (S1/S2)** and **PC (PC1/PC2)**:

---

```markdown
# 📘 2.7.6 - Implement Basic Connectivity

This file contains **all commands** and **manual configuration steps** for setting up basic connectivity between switches and PCs in Cisco Packet Tracer.

---

## 📁 Project Structure

```

2.7.6-Implement-Basic-Connectivity/
│
├── Switches/
│   ├── S1/
│   │   ├── Basic Config
│   │   ├── VLAN 1 Interface Setup
│   │   └── IP Verification
│   └── S2/
│       ├── Basic Config
│       ├── VLAN 1 Interface Setup
│       └── IP Verification
│
├── PCs/
│   ├── PC1/
│   │   └── Manual IP + Ping Test
│   └── PC2/
│       └── Manual IP + Ping Test

````

---

## 🔌 Switch Configuration (S1 and S2)

> 💻 Fired from: Switch CLI (S1 or S2 Terminal)

### ✅ Step 1: Basic Configuration

```bash
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1          # Use S2 for second switch
S1(config)# line console 0
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)# exit
S1(config)# enable secret class
S1(config)# banner motd #Unauthorized access is prohibited#
S1(config)# end
S1# write memory
````

### ✅ Step 2: VLAN Interface Setup

```bash
S1# configure terminal
S1(config)# interface vlan 1
S1(config-if)# ip address 192.168.1.253 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# exit
S1(config)# end
S1# write memory
```

> 🔁 Repeat same steps for S2 with IP: `192.168.1.254`

---

## 💻 PC Configuration

> 📍 Fired from: GUI on PC (Desktop > IP Configuration)

### ✅ PC1:

```plaintext
IP Address:      192.168.1.1
Subnet Mask:     255.255.255.0
Default Gateway: [Leave Blank]
```

### ✅ PC2:

```plaintext
IP Address:      192.168.1.2
Subnet Mask:     255.255.255.0
Default Gateway: [Leave Blank]
```

---

## 🔍 IP Address Verification

> 💻 Fired from: **Windows Command Prompt on PC1 or PC2**

```bash
C:\> ipconfig
```

You should see:

```plaintext
IPv4 Address. . . . . . . . . . . : 192.168.1.1
Subnet Mask . . . . . . . . . . . : 255.255.255.0
Default Gateway . . . . . . . . . : 
```

---

## 🧪 Ping Tests

> 🧪 Fired from: **PC1 Command Prompt**

```bash
ping 192.168.1.2       # Ping PC2
ping 192.168.1.253     # Ping Switch S1
ping 192.168.1.254     # Ping Switch S2
```

> 🧪 Fired from: **PC2 Command Prompt**

```bash
ping 192.168.1.1       # Ping PC1
```

---

## 📊 Show Commands on Switch

> 🔧 Fired from: Switch CLI (S1 or S2)

```bash
S1# show ip interface brief
S1# show running-config
```

---

✅ This confirms successful manual IP configuration and device connectivity in a basic LAN setup.

```

---

Would you like me to export this as a `.md` file for your project folder?
```

