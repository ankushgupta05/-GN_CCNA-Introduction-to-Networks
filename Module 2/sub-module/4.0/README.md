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
