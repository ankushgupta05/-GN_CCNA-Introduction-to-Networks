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



## 🧪 2.2.7 Syntax Checker – Navigate Between IOS Modes (With Real-Life Examples)

This activity helps you practice moving between Cisco IOS modes using real commands. Here's a step-by-step breakdown with simple daily life comparisons.

| Step | Command                        | IOS Mode Entered                     | Prompt                        | Real-Life Example                                                       |
|------|--------------------------------|--------------------------------------|-------------------------------|-------------------------------------------------------------------------|
| 1    | `enable`                       | Privileged EXEC Mode                 | `Switch#`                     | Like unlocking your phone to access all settings.                       |
| 2    | `disable`                      | Back to User EXEC Mode               | `Switch>`                     | Like locking your phone screen again.                                   |
| 3    | `enable`                       | Privileged EXEC Mode                 | `Switch#`                     | Unlocking it again.                                                     |
| 4    | `configure terminal`           | Global Configuration Mode            | `Switch(config)#`             | Entering system settings to make device-wide changes.                   |
| 5    | `exit`                         | Back to Privileged EXEC Mode         | `Switch#`                     | Pressing “Back” from settings.                                          |
| 6    | `configure terminal`           | Global Configuration Mode            | `Switch(config)#`             | Re-entering settings.                                                   |
| 7    | `line console 0`               | Line Config Mode (Console)           | `Switch(config-line)#`        | Going into screen lock settings.                                        |
| 8    | `exit`                         | Back to Global Configuration Mode    | `Switch(config)#`             | Back to main settings menu.                                             |
| 9    | `line vty 0 15`                | Line Config Mode (VTY - SSH/Telnet)  | `Switch(config-line)#`        | Going into remote access settings.                                      |
| 10   | `exit`                         | Back to Global Configuration Mode    | `Switch(config)#`             | Again, back to main settings.                                           |
| 11   | `interface vlan 1`             | Interface Config Mode                | `Switch(config-if)#`          | Configuring a specific network interface.                               |
| 12   | `line console 0`               | Line Config Mode (Console again)     | `Switch(config-line)#`        | Switching from Wi-Fi settings to screen lock settings directly.         |
| 13   | `exit`                         | Back to Global Configuration Mode    | `Switch(config)#`             | Back to main settings.                                                  |
| 14   | `end`                          | Back to Privileged EXEC Mode         | `Switch#`                     | Exiting all settings to the main admin screen.                          |

✅ **You successfully navigated through different Cisco IOS command line modes!**

> 🧠 Tip: Think of IOS modes like nested menus in your phone's settings – each step gets you deeper into specific options, and each exit or end takes you back a level or all the way out.




## ✅ 2.2.8 Check Your Understanding – IOS Navigation

### Question 1  
Which IOS mode allows access to all commands and features?

Option | Answer | Explanation  
------ | ------ | -----------  
🅐 Global configuration mode | ❌ Incorrect | This mode allows setting device-wide configurations, but not all commands/features are accessible here.  
🅑 Interface subconfiguration mode | ❌ Incorrect | This is a specific part of configuration, not where full access is granted.  
🅒 Line console subconfiguration mode | ❌ Incorrect | This is for line settings only, limited scope.  
🅓 Privileged EXEC mode | ✅ Correct | This mode allows access to all monitoring, configuration, and management commands.  
🅔 User EXEC mode | ❌ Incorrect | View-only mode; limited command access.  
🔹 Example: Needed to enter configuration mode using `configure terminal`.  
🔹 Use: Full admin control of the device.

---

### Question 2  
Which IOS mode are you in if the `Switch(config)#` prompt is displayed?

Option | Answer | Explanation  
------ | ------ | -----------  
🅐 Global configuration mode | ✅ Correct | The `(config)#` prompt indicates global configuration mode.  
🅑 Interface subconfiguration mode | ❌ Incorrect | Would show `(config-if)#` in prompt.  
🅒 Line console subconfiguration mode | ❌ Incorrect | Would show `(config-line)#`.  
🅓 Privileged EXEC mode | ❌ Incorrect | Shows as `Switch#`, no `(config)` in prompt.  
🅔 User EXEC mode | ❌ Incorrect | Shows as `Switch>`.  
🔹 Example: `Switch# configure terminal` takes you here.  
🔹 Use: To configure device-wide settings.

---

### Question 3  
Which IOS mode are you in if the `Switch>` prompt is displayed?

Option | Answer | Explanation  
------ | ------ | -----------  
🅐 Global configuration mode | ❌ Incorrect | Would show `Switch(config)#`.  
🅑 Interface subconfiguration mode | ❌ Incorrect | Would show `Switch(config-if)#`.  
🅒 Line console subconfiguration mode | ❌ Incorrect | Would show `Switch(config-line)#`.  
🅓 Privileged EXEC mode | ❌ Incorrect | Would show `Switch#`.  
🅔 User EXEC mode | ✅ Correct | The `>` symbol indicates User EXEC mode.  
🔹 Example: First mode after accessing the CLI.  
🔹 Use: Limited commands like `ping` or `show`.

---

### Question 4  
Which two commands would return you to the **privileged EXEC** prompt regardless of the configuration mode you are in? (Choose two.)

Option | Answer | Explanation  
------ | ------ | -----------  
🅐 CTRL+Z | ✅ Correct | This shortcut exits all modes and returns to privileged EXEC.  
🅑 disable | ❌ Incorrect | This returns you to user EXEC, not privileged EXEC.  
🅒 enable | ❌ Incorrect | Used to *enter* privileged EXEC from user EXEC, not to return to it.  
🅓 end | ✅ Correct | This command ends all configuration modes and returns to privileged EXEC.  
🅔 exit | ❌ Incorrect | This exits one level up, not always directly to privileged EXEC.  
🔹 Example: Use `end` or `Ctrl+Z` to return quickly to privileged EXEC mode.  
🔹 Use: Helps you skip multiple "exit" steps.

---



## ✅ 2.3.2 IOS Command Syntax Check

Understanding how to read and interpret IOS command syntax is essential for configuring Cisco devices accurately. Below is a breakdown of command documentation conventions and examples.

### 📘 Syntax Conventions

| Convention | Meaning | Example | Explanation |
|-----------|---------|---------|-------------|
| **boldface** | Literal commands and keywords entered exactly as shown | **ping** | Type the command exactly as written |
| *italics* | User-supplied argument | *ip-address* | You provide a value, like 192.168.1.1 |
| [x] | Optional element | [vrf NAME] | You may include it, but it's not required |
| {x} | Required choice between options | {static \| dynamic} | Must choose one of the enclosed options |
| [x {y \| z}] | Optional element with required choice | [mode {access \| trunk}] | Optional as a whole, but if used, one choice is required |

---

### 📘 Example Command: `description string`

| Syntax | Explanation |
|--------|-------------|
| **description** *string* | `description` is the literal command. `string` is a user-supplied description for the interface. |
| 🔹 Example: | `description Connects to the main headquarter office switch` |

---

### 📘 Other Examples

| Command | Explanation |
|--------|-------------|
| **ping** *ip-address* | Sends ICMP Echo Requests to the specified IP. |
| 🔹 Example: | `ping 10.10.10.5` |
| **traceroute** *ip-address* | Traces the route packets take to reach the IP. |
| 🔹 Example: | `traceroute 192.168.254.254` |

---

### 📘 Complex Command Example

```bash
Switch(config-if)# switchport port-security aging { static | time time | type {absolute | inactivity} }

