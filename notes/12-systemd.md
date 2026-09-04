# Lesson 12 - Managing System Startup Services with Systemd

## Summary

This lesson introduced systemd, which is used to manage services and control what starts when a Linux system boots.

---

## Key Concepts

- systemd manages services and system startup.
- It decides what gets started, when it starts, and in what order.
- systemd uses units to manage different parts of the system.
- Service units are used to manage applications and daemons.
- Socket units are used to activate services on demand.
- Timer units are used to schedule tasks.
- Path units are used to monitor files and directories.
- Target units are used to group units together.

---

## Commands Learned

    dnf install -y httpd
    echo "hello world" | tee /var/www/html/index.html
    systemctl start httpd
    systemctl enable httpd
    systemctl enable --now httpd
    systemctl status httpd
    systemctl restart httpd
    systemctl stop httpd
    systemctl disable httpd
    firewall-cmd --add-service=http
    firewall-cmd --permanent --add-service=http
    firewall-cmd --list-all

---

## Notes

### What is systemd?

systemd is used to manage services and system startup in Linux.

It decides:

- What services should start.
- When services should start.
- The order in which services should start.
- Which services should continue running.

---

### systemd Units

systemd manages the system using different types of units.

#### Service Units

Service units are used for running applications and daemons.

Example:

    httpd.service

#### Socket Units

Socket units activate services on demand when they are needed.

#### Timer Units

Timer units are used to schedule tasks.

#### Path Units

Path units monitor files or directories for changes.

#### Target Units

Target units group related units together.

---

### Managing the HTTPD Service

A web server can be installed and managed using systemd.

Install HTTPD:

    dnf install -y httpd

Create a simple web page:

    echo "hello world" | tee /var/www/html/index.html

Start the service:

    systemctl start httpd

Enable the service so it starts automatically at boot:

    systemctl enable httpd

Start and enable the service at the same time:

    systemctl enable --now httpd

Check the status of the service:

    systemctl status httpd

---

### Managing Services

#### Start

    systemctl start httpd

Starts the service immediately.

#### Stop

    systemctl stop httpd

Stops the service.

#### Restart

    systemctl restart httpd

Restarts the service.

This is useful after changing a service's configuration.

#### Enable

    systemctl enable httpd

Configures the service to start automatically when the system boots.

#### Disable

    systemctl disable httpd

Prevents the service from starting automatically at boot.

---

### Managing the Firewall

A web server needs HTTP traffic to be allowed through the firewall.

Allow HTTP temporarily:

    firewall-cmd --add-service=http

Make the rule permanent:

    firewall-cmd --permanent --add-service=http

View the firewall configuration:

    firewall-cmd --list-all

---

### Configuration Changes

If you change a service's configuration file, the service may need to be restarted for the changes to take effect.

Example:

    systemctl restart httpd

---

## What I Learned

I learned that systemd is responsible for managing services and controlling system startup in Linux.

I learned how to start, stop, restart, enable, and disable services using `systemctl`. I also learned how `firewall-cmd` can be used to allow HTTP traffic through the firewall when running a web server.
