# Lab 17 - Managing Systems with the RHEL Web Console

## Objective

Practice enabling and accessing the RHEL Web Console (Cockpit) and exploring its available plugins.

---

## Tasks Completed

- Learned what Cockpit is.
- Enabled the Cockpit socket.
- Accessed Cockpit through a web browser.
- Explored the web-based administration dashboard.
- Learned what types of system tasks can be managed through Cockpit.
- Searched for available Cockpit plugins.

---

## Commands Used

Enable and start Cockpit:

    sudo systemctl enable --now cockpit.socket

Access Cockpit:

    http://localhost:9090

Search for Cockpit plugins:

    dnf search cockpit-*

---

## Practice

I enabled the Cockpit socket and accessed the RHEL Web Console through a browser.

I explored the dashboard and learned how Cockpit provides a graphical way to manage system administration tasks.

I also searched for available Cockpit plugins that can extend the functionality of the web console.

---

## Outcome

I learned how Cockpit provides a web-based alternative to managing RHEL systems through the command line.

I can now enable Cockpit, access the web console, and search for additional plugins that can help with system administration.