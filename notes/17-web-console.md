# Lesson 17 - Managing Systems with the RHEL Web Console

## Summary

This lesson introduced the RHEL Web Console, also known as Cockpit. It is a web-based dashboard that allows administrators to manage RHEL systems through a browser.

---

## Key Concepts

- The RHEL Web Console is also known as **Cockpit**.
- Cockpit is a web-based dashboard built into RHEL.
- It allows administrators to perform system administration tasks through a web browser.
- Cockpit can be accessed from different devices, including mobile browsers.
- It provides a graphical alternative to managing RHEL through the command line.
- Cockpit can be extended with additional plugins.
- Cockpit uses the same underlying Linux tools and services that can be managed from the command line.

---

## Commands Learned

    sudo systemctl enable --now cockpit.socket
    dnf search cockpit-*
    sudo dnf install -y cockpit-*

---

## Notes

### What is Cockpit?

Cockpit is a web-based administration dashboard for RHEL.

It allows administrators to manage systems through a browser instead of using only the command line.

Cockpit can be accessed from:

- Desktop browsers
- Laptop browsers
- Mobile browsers

---

### Enabling Cockpit

Cockpit can be enabled using:

    sudo systemctl enable --now cockpit.socket

This starts the Cockpit socket immediately and enables it to start automatically.

---

### Accessing the Web Console

Once Cockpit is running, it can be accessed through:

    http://localhost:9090

Port `9090` is used by the Cockpit web interface.

---

### Why Use Cockpit?

Cockpit provides a visual way to perform many of the same administration tasks available through the command line.

It can make system administration easier for people who prefer to visualize system information.

Cockpit can help administrators manage:

- System information
- Services
- Storage
- Networking
- Logs
- Users
- Other system tools

---

### Cockpit Plugins

Cockpit can be extended with additional plugins.

Search for available Cockpit packages:

    dnf search cockpit-*

Install a Cockpit plugin:

    sudo dnf install -y cockpit-*

The available plugins can provide additional functionality for managing different parts of a RHEL system.

---

## What I Learned

I learned that Cockpit provides a web-based interface for managing RHEL systems.

I learned how to enable the Cockpit service, access it through a web browser, and search for additional Cockpit plugins.

Cockpit provides a visual alternative to the command line while still allowing administrators to manage the same underlying Linux system.

---

## Questions

- What can I manage in Cockpit that I can also manage with the command line?
- What Cockpit plugins are available for RHEL?
- How is Cockpit secured when accessing it remotely?