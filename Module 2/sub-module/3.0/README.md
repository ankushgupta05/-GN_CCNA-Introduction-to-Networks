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



## 🔄 2.2.4 Navigating Between Cisco IOS Modes – With Daily Life Examples

Cisco IOS uses different modes for different tasks. Knowing how to move between these modes is essential for configuration.

### 🧭 Common Navigation Commands

| Action                                      | Command                        | Moves You To               | Prompt Changes To          | Daily Life Example                                                         |
|---------------------------------------------|--------------------------------|-----------------------------|-----------------------------|------------------------------------------------------------------------------|
| Enter Privileged EXEC mode                 | `enable`                       | From User EXEC to Privileged | `Switch#`                  | Like unlocking your phone to access admin settings.                         |
| Exit to User EXEC mode                     | `disable`                      | From Privileged to User EXEC | `Switch>`                  | Like locking your phone screen after you're done.                           |
| Enter Global Configuration mode            | `configure terminal`           | From Privileged EXEC         | `Switch(config)#`          | Like entering your phone's full settings menu.                              |
| Exit Global Config to Privileged EXEC      | `exit`                         | From Global Config           | `Switch#`                  | Like pressing "Back" to return to the previous screen.                      |
| Enter Line Configuration mode              | `line console 0`               | From Global Config           | `Switch(config-line)#`     | Like going into lock screen settings specifically.                          |
| Exit Line Config to Global Config          | `exit`                         | From Line Config             | `Switch(config)#`          | Like exiting from Wi-Fi settings back to general settings.                 |
| Enter Interface Configuration mode         | `interface FastEthernet 0/1`   | From Global Config           | `Switch(config-if)#`       | Like adjusting settings for a specific app or feature on your phone.       |
| Exit All the Way to Privileged EXEC Mode   | `end` or `Ctrl + Z`            | From Any Submode             | `Switch#`                  | Like hitting the home button to go back to the main screen from deep inside. |

### 🧠 Quick Tip:
- Use `exit` to go **one step up**.
- Use `end` or `Ctrl + Z` to go **all the way back** to Privileged EXEC mode from any depth.

This system helps keep your configurations organized and controlled — just like navigating different menus and settings on your smartphone.

