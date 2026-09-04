# Systemd Commands

## Install HTTPD

    dnf install -y httpd

---

## Start a Service

    systemctl start httpd

Starts the service immediately.

---

## Stop a Service

    systemctl stop httpd

Stops a running service.

---

## Restart a Service

    systemctl restart httpd

Restarts a service after configuration changes.

---

## Enable a Service

    systemctl enable httpd

Configures the service to start automatically at boot.

---

## Enable and Start a Service

    systemctl enable --now httpd

Starts the service immediately and enables it to start at boot.

---

## Check Service Status

    systemctl status httpd

Displays the current status of a service.

---

## Disable a Service

    systemctl disable httpd

Prevents a service from starting automatically at boot.

---

## Create a Simple Web Page

    echo "hello world" | tee /var/www/html/index.html

---

## Allow HTTP Through the Firewall

    firewall-cmd --add-service=http

---

## Make the Firewall Rule Permanent

    firewall-cmd --permanent --add-service=http

---

## View Firewall Configuration

    firewall-cmd --list-all

---

## systemd Unit Types

    service = Runs applications and daemons
    socket  = Activates services on demand
    timer   = Schedules tasks
    path    = Watches files and directories
    target  = Groups units together