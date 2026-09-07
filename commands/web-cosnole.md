# RHEL Web Console / Cockpit Commands

## Enable and Start Cockpit

    sudo systemctl enable --now cockpit.socket

---

## Access Cockpit

    http://localhost:9090

---

## Search for Cockpit Packages

    dnf search cockpit-*

---

## Install Cockpit Plugins

    sudo dnf install -y cockpit-*