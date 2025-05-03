# 2.4.1 Device Names

When configuring a Cisco IOS device for the first time, the **first step** should be assigning it a **unique and descriptive hostname**. By default, Cisco switches are named `Switch`, which can lead to confusion when managing multiple devices, especially over remote access like SSH.

## Why Use Hostnames?

- Helps confirm you're connected to the correct device.
- Simplifies documentation and troubleshooting.
- Makes it easier to identify devices by location or purpose.

### Example Naming Convention

A switch on each floor of a building might be named:

- `Sw-Floor-1`
- `Sw-Floor-2`
- `Sw-Floor-3`

This makes it clear which floor each switch belongs to.

## Hostname Rules

Hostnames must:
- Start with a **letter**
- End with a **letter or digit**
- Contain **no spaces**
- Use only **letters, digits, and dashes (-)**
- Be **less than 64 characters**

> **Note:** Hostnames are case-sensitive in Cisco IOS.

## Setting the Hostname (Cisco CLI)

Use the following commands:

```bash
Switch# configure terminal
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)#

```


Here is the updated `README.md` content for **sections 2.4.2 to 2.4.5** including examples for each concept, while keeping the original content intact:

---

````markdown
# 2.4.2 Password Guidelines

Weak or easily guessed passwords remain one of the biggest security vulnerabilities. All network devices—including home routers—should always require a password for administrative access.

Cisco IOS supports **hierarchical passwords** to grant different access levels. Always secure the following modes:
- **User EXEC**
- **Privileged EXEC**
- **Remote Telnet/SSH**

### Password Best Practices

- Use **more than eight characters**
- Combine **uppercase, lowercase, digits, and special characters**
- Avoid reusing the same password across devices
- Avoid common words or predictable patterns
- Consider using an online **password generator**

> ⚠️ **Note:** Labs in this course may use weak passwords (like `cisco` or `class`) for simplicity. These should never be used in production environments.

### ✅ Example: Strong Password
```bash
# Instead of using weak password like: cisco
# Use something strong like:
Pa$$w0rd!2025
````

---

# 2.4.3 Configure Passwords

When connecting to a Cisco device for the first time, you're placed in **user EXEC mode**. Here’s how to secure it:

## 🔐 Secure Console Access (User EXEC Mode)

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line console 0
Sw-Floor-1(config-line)# password Cisco123!
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

## 🔐 Secure Privileged EXEC Mode

This mode allows full device configuration. Use `enable secret`:

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# enable secret StrongEnablePass!
Sw-Floor-1(config)# exit
Sw-Floor-1#
```

## 🔐 Secure Remote Access (VTY Lines)

Most Cisco devices support 16 VTY lines (0 to 15). Secure them using:

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password Remote$Access123
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

---

# 2.4.4 Encrypt Passwords

By default, passwords in the running or startup config are stored in plaintext. To prevent this:

## 🔐 Apply Encryption to Passwords

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# service password-encryption
Sw-Floor-1(config)#
```

This uses **weak encryption** (type 7), but it hides passwords from casual viewing.

## 🔍 Verify Encrypted Passwords

```bash
Sw-Floor-1# show running-config
!
line con 0
password 7 14141B180F0B
login
!
line vty 0 4
password 7 0A1E1C485C081E
login
line vty 5 15
password 7 061F4B1C1B1C
login
!
```

### 📝 Example Before and After

```bash
# Before encryption
password Remote$Access123

# After service password-encryption
password 7 061F4B1C1B1C
```

---

# 2.4.5 Banner Messages

A banner displays a **message of the day (MOTD)** when accessing the device. This is useful for legal notification and access warnings.

## 🛑 Configure Banner MOTD

Use the `banner motd` command with a delimiter:

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# banner motd #Unauthorized Access is Prohibited. Violators will be prosecuted.#
```

* The `#` character is the delimiter (you can use any character that **does not appear in the message**).
* The message will display to **all users on login**.

### 💡 Example Output on Login

```bash
Unauthorized Access is Prohibited. Violators will be prosecuted.
```

> ✅ Tip: Banner messages are sometimes required to enforce monitoring and prosecution policies in legal systems.

---

```

Would you like me to export this as a downloadable `README.md` file for your project?
```



## 🔐 Cisco Password Setup Summary

In a Cisco device, there are **three main places** where passwords are needed for security:

---

### 1️⃣ Console Password (`line console 0`)

This is the **physical port** (jaise direct cable se connected PC). Isse secure karne ke liye:

```bash
Sw(config)# line console 0
Sw(config-line)# password MyConsole123
Sw(config-line)# login
```

🗣️ *Simple Bhasha*: Jab aap **seedha device ke saath baithe ho** (wire laga ke), to yeh password puchega.

---

### 2️⃣ Remote Access Password (`line vty 0 15`)

Yeh hota hai jab aap **door se (telnet/SSH)** se device access karte ho.

```bash
Sw(config)# line vty 0 15
Sw(config-line)# password MyRemote@123
Sw(config-line)# login
```

🗣️ *Simple Bhasha*: Jab aap **remotely (network ke zariye)** device me login karte ho, to yeh password lagega. `0 15` ka matlab hai — 16 log ek saath connect ho sakte hain.

---

### 3️⃣ Privileged Mode Password (`enable secret`)

Yeh sabse powerful mode hota hai jahan aap device ki puri configuration kar sakte ho.

```bash
Sw(config)# enable secret MyAdmin@321
```

🗣️ *Simple Bhasha*: Jab aap “enable” likh ke **admin mode me jaate ho**, tab yeh password maanga jaata hai. Yeh encrypted hota hai aur secure hota hai.

---

✅ **Quick Recap Table**

| Mode             | Command Example                       | Used When...                        |
|------------------|----------------------------------------|-------------------------------------|
| Console Access   | `line console 0`                       | Direct cable se device control karte ho |
| Remote Access    | `line vty 0 15`                        | Telnet/SSH se device control karte ho |
| Admin Privilege  | `enable secret MyAdmin@321`           | Full configuration access chahiye hota hai |

---

> 🔐 Tip: Hamesha strong password use karo jisme capital, small letters, numbers, aur special characters ho.

