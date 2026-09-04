# Networking Commands

## View Network Profiles

    nmcli con show

Short version:

    nmcli c s

---

## View a Specific Connection

    nmcli con show <profilename>

Example:

    nmcli con show datacenter

---

## View Network Interfaces

    ip address show

Short version:

    ip a s

View a specific interface:

    ip a s enp7s0

---

## Create a Static Network Profile

    nmcli connection add con-name datacenter type ethernet ifname enp7s0 ipv4.method manual ipv4.address "192.168.1.114/24" ipv4.gateway 192.168.1.1 ipv4.dns "1.1.1.1"

---

## Check Routing and Gateway

    ip r s

---

## Check DNS Configuration

    cat /etc/resolv.conf

---

## Delete a Connection

    nmcli con del datacenter

---

## NetworkManager Text Interface

    nmtui

Use `nmtui` to add, edit, and remove network profiles without having to remember long `nmcli` commands.

---

## Useful NetworkManager Tip

Use Tab completion while working with `nmcli`:

    nmcli
    nmcli connection
    nmcli connection add