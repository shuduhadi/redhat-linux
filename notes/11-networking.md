# Lesson 11 - Managing Networking

## Summary

This lesson introduced Linux networking and how NetworkManager makes it easier to configure and manage network interfaces and connection profiles.

---

## Key Concepts

- Linux networking is managed using **NetworkManager**.
- Network devices are represented as network interfaces.
- Interface names can include `eth0`, `enp1s0`, or `wlp2s0`.
- NetworkManager organizes network settings into profiles, which are sometimes called connections.
- A connection profile contains properties and values that control how an interface behaves.
- An interface can only have one active profile at a time.
- `nmcli` is a command-line tool used to manage NetworkManager.
- `nmtui` provides a more user-friendly interface for managing network profiles.

---

## Commands Learned

    nmcli con show
    nmcli c s
    nmcli con show <profilename>
    ip address show
    ip a s
    ip a s enp7s0
    ip r s
    cat /etc/resolv.conf
    nmcli con del datacenter
    nmtui

---

## Notes

### Network Interfaces

Network devices are represented in Linux as **network interfaces**.

Examples include:

    eth0
    enp1s0
    wlp2s0

The naming depends on the system's hardware and Linux naming conventions.

### Interface Naming

For example:

    enp7s0

The name can be broken down into:

- `en` = Ethernet
- `p7` = port 7
- `s0` = slot 0

---

### NetworkManager

NetworkManager makes managing Linux networking easier.

It organizes network settings into **profiles**, which are also called connections.

A profile contains a set of properties and values that control how an interface behaves.

Important points:

- A single profile supplies settings to a single interface.
- An interface can only have one active profile at a time.
- Profiles can be created, edited, activated, and deleted.

---

### Display Network Profiles

To display all NetworkManager profiles:

    nmcli con show

A shorter version is:

    nmcli c s

---

### View a Specific Profile

To see the settings inside a specific connection profile:

    nmcli con show <profilename>

Example:

    nmcli con show datacenter

---

### View Network Interfaces

To see the current network interfaces and their settings:

    ip address show

A shorter version is:

    ip a s

To view a specific interface:

    ip a s enp7s0

---

### Creating a Static Network Profile

A connection profile can be created with a static IP address.

Example:

    nmcli connection add con-name datacenter type ethernet ifname enp7s0 ipv4.method manual ipv4.address "192.168.1.114/24" ipv4.gateway 192.168.1.1 ipv4.dns "1.1.1.1"

This creates a profile called `datacenter` for the `enp7s0` Ethernet interface.

The profile is configured with:

- Static IPv4 addressing
- IP address: `192.168.1.114/24`
- Gateway: `192.168.1.1`
- DNS server: `1.1.1.1`

---

### Checking the IP Address

To check the IP address assigned to an interface:

    ip a s enp7s0

---

### Checking the Gateway

To view the routing table and check the gateway:

    ip r s

---

### Checking DNS

To view the current DNS configuration:

    cat /etc/resolv.conf

---

### Deleting a Connection Profile

To delete the `datacenter` connection:

    nmcli con del datacenter

---

### nmtui

`nmtui` is a text-based, user-friendly tool for managing NetworkManager.

It can be used to:

- Add network profiles
- Edit network profiles
- Remove network profiles

It is useful when you do not want to remember long `nmcli` commands.

---

### Tab Completion

NetworkManager commands can become long and difficult to remember.

A useful tip is to use **Tab completion** while typing commands.

For example:

    nmcli<Tab>
    nmcli connection<Tab>
    nmcli connection add<Tab>

Pressing Tab can show available commands and options and help you complete the command.

---

## What I Learned

I learned how Linux represents network hardware using interfaces and how NetworkManager uses connection profiles to manage network settings.

I also learned how to use `nmcli` to view, create, and delete network profiles and how to use commands such as `ip a`, `ip r`, and `/etc/resolv.conf` to check network configuration.
