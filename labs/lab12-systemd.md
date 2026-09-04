# Lab 12 - Managing System Startup Services with Systemd

## Objective

Practice managing a service with systemd and configuring the firewall to allow HTTP traffic.

---

## Tasks Completed

- Installed the Apache HTTP server.
- Created a simple web page.
- Started the HTTPD service.
- Enabled HTTPD to start automatically at boot.
- Checked the service status.
- Added HTTP to the firewall.
- Reviewed the firewall configuration.
- Practiced stopping and restarting the service.

---

## Commands Used

Install HTTPD:

    dnf install -y httpd

Create a web page:

    echo "hello world" | tee /var/www/html/index.html

Start HTTPD:

    systemctl start httpd

Enable HTTPD at boot:

    systemctl enable httpd

Start and enable HTTPD together:

    systemctl enable --now httpd

Check the service:

    systemctl status httpd

Allow HTTP through the firewall:

    firewall-cmd --add-service=http

Make the firewall rule permanent:

    firewall-cmd --permanent --add-service=http

View firewall rules:

    firewall-cmd --list-all

Restart HTTPD:

    systemctl restart httpd

Stop HTTPD:

    systemctl stop httpd

---

## Practice

I practiced using `systemctl` to control the HTTPD service.

I started and stopped the service, checked its status, and enabled it to start automatically when the system boots.

I also practiced configuring the firewall to allow HTTP traffic.

---

## Outcome

I learned how systemd manages services and startup processes in Linux. I can now use `systemctl` to control services and `firewall-cmd` to manage firewall rules for a web server.