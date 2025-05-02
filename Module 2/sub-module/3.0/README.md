## ✅ 2.2.1 Primary Command Modes – Explained with Daily Life Examples

Cisco devices have two main modes in CLI (Command Line Interface):

| Command Mode         | Prompt Symbol | Description                                                                                  | Daily Life Example                                                                 |
|----------------------|----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **User EXEC Mode**   | `>`            | - Basic mode<br>- Only allows view or monitoring commands<br>- No configuration allowed     | Like entering a bank to check your account balance – you can see info but not change it. |
| **Privileged EXEC Mode** | `#`      | - Full access to all commands<br>- Allows configuration and management commands             | Like being the bank manager – you can change account settings, not just view them. |

### 🧠 Summary:
- `Switch>` or `Router>` means **User EXEC Mode** (view-only).
- `Switch#` or `Router#` means **Privileged EXEC Mode** (full control).

You must switch to **Privileged EXEC Mode** to configure devices.



## ⚙️ 2.2.2 Configuration and Subconfiguration Modes – With Daily Life Examples

To **configure a Cisco device**, you need to go beyond just viewing settings. You must enter **Global Configuration Mode**, and from there, you can access more specific settings through **Subconfiguration Modes**.

### 🧾 Modes Overview

| Mode                         | Prompt Example             | Description                                                                                 | Daily Life Example                                                                 |
|------------------------------|----------------------------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Global Configuration Mode** | `Switch(config)#`          | Used to change overall settings on the device.                                              | Like going into the settings menu of your phone to change general preferences.     |
| **Line Configuration Mode**   | `Switch(config-line)#`     | Used to configure access methods like console, SSH, or Telnet.                              | Like changing the way you unlock your phone – password, fingerprint, or face ID.   |
| **Interface Configuration Mode** | `Switch(config-if)#`   | Used to configure a specific port or interface on the switch or router.                    | Like changing Wi-Fi settings for one specific network in your phone.               |

### 🧠 Summary:
- All configuration starts from **Global Config Mode**.
- From there, you go into more detailed settings using **Subconfiguration Modes**.
- The **prompt changes** depending on which mode you're in:
  - Global: `(config)#`
  - Line: `(config-line)#`
  - Interface: `(config-if)#`

This structure helps keep things organized and focused when configuring different parts of a Cisco device.
