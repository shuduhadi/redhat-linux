# Lab 13 - Deploying an Application Runtime

## Objective

Practice deploying a simple Node.js application on RHEL and managing it as a systemd service.

---

## Tasks Completed

- Installed Node.js.
- Cloned a Node.js application from Git.
- Inspected the application files.
- Viewed `package.json`.
- Installed the application's dependencies.
- Installed the systemd service file.
- Reloaded systemd.
- Started and enabled the application.
- Checked the application service status.
- Opened port 8080 in the firewall.
- Tested the application in Firefox.

---

## Commands Used

Install Node.js:

    sudo dnf install -y nodejs

Clone the application:

    git clone https://gitlab.com/rgdacosta/nodejs_rhel10.git

Enter the application directory:

    cd nodejs_rhel10/

List the files:

    ls

View package.json:

    cat package.json

Install dependencies:

    npm install

Copy the service file:

    sudo cp myapp.service /etc/systemd/system/

Reload systemd:

    sudo systemctl daemon-reload

Start and enable the service:

    sudo systemctl enable --now myapp

Check the service:

    systemctl status myapp

Allow port 8080:

    sudo firewall-cmd --add-port=8080/tcp

Make the firewall rule permanent:

    sudo firewall-cmd --permanent --add-port=8080/tcp

---

## Practice

I practiced deploying a Node.js application on RHEL.

I installed Node.js, cloned the application repository, installed the required dependencies, and configured the application as a systemd service.

I also configured the firewall to allow traffic on port 8080 and tested the application using Firefox.

---

## Outcome

I learned how to deploy a simple application and manage it as a Linux service using systemd.

The application can now start automatically when the system boots and can be managed using standard systemd commands.