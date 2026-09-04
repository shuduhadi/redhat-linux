# Lab 11 - Managing Networking

## Objective

Practice viewing network interfaces, inspecting NetworkManager profiles, and understanding how network connections are configured.

---

## Tasks Completed

- Listed available NetworkManager connection profiles.
- Viewed the settings of a connection profile.
- Listed current network interfaces.
- Checked the IP address of a network interface.
- Checked the routing table and gateway.
- Checked the DNS configuration.
- Explored `nmtui` for managing network profiles.

---

## Commands Used

View connection profiles:

    nmcli con show

View a specific profile:

    nmcli con show <profilename>

View network interfaces:

    ip a s

View a specific interface:

    ip a s enp7s0

Check the routing table:

    ip r s

Check DNS:

    cat /etc/resolv.conf

Open the NetworkManager text interface:

    nmtui

---

## Practice

I practiced using `nmcli` to view NetworkManager connection profiles.

I used `ip a s` to inspect network interfaces and their IP addresses.

I also used `ip r s` to view the routing table and `cat /etc/resolv.conf` to check the DNS configuration.

I explored `nmtui` as an alternative way to manage network profiles.

---

## Outcome

I learned how Linux represents network devices as interfaces and how NetworkManager uses connection profiles to manage them.

I also learned how to inspect IP addresses, gateways, and DNS settings using Linux networking commands.