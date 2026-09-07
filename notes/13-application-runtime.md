# Lesson 13 - Deploying an Application Runtime to Host a Simple Application

## Summary

This lesson demonstrated how to deploy a Node.js application on RHEL 10 and manage it as a systemd service. Using systemd allows the application to start automatically at boot, restart after failures, and be managed like other Linux services.

---

## Key Concepts

- Applications can be managed as systemd services.
- Node.js can be installed using `dnf`.
- An application can be downloaded from a Git repository using `git clone`.
- `npm install` installs the dependencies required by a Node.js application.
- A systemd service file can be used to manage the application.
- `systemctl enable --now` can start a service immediately and enable it at boot.
- Systemd can help an application recover from crashes and manage its logging.
- A firewall rule is required to allow access to the application's port.

---

## Commands Learned

    sudo dnf install -y nodejs
    git clone https://gitlab.com/rgdacosta/nodejs_rhel10.git
    cd nodejs_rhel10/
    ls
    cat package.json
    npm install
    sudo cp myapp.service /etc/systemd/system/
    sudo systemctl daemon-reload
    sudo systemctl enable --now myapp
    systemctl status myapp
    sudo firewall-cmd --add-port=8080/tcp
    sudo firewall-cmd --permanent --add-port=8080/tcp

---

## Notes

### Installing Node.js

Install Node.js using `dnf`:

    sudo dnf install -y nodejs

The `-y` option automatically confirms the installation.

---

### Getting the Application

Clone the application repository:

    git clone https://gitlab.com/rgdacosta/nodejs_rhel10.git

Move into the application directory:

    cd nodejs_rhel10/

List the files:

    ls

View the Node.js project configuration:

    cat package.json

---

### Installing Dependencies

Node.js applications can require additional packages called dependencies.

Install the dependencies listed in `package.json`:

    npm install

---

### Creating a systemd Service

The application includes a systemd service file called `myapp.service`.

Copy the service file into the systemd service directory:

    sudo cp myapp.service /etc/systemd/system/

This makes the service available to systemd.

---

### Reloading systemd

After adding or changing a systemd service file, systemd needs to reload its configuration:

    sudo systemctl daemon-reload

---

### Starting and Enabling the Application

Start the application and enable it to start automatically at boot:

    sudo systemctl enable --now myapp

This performs two actions:

- Starts the application immediately.
- Enables the application to start automatically when the system boots.

---

### Checking the Service

Check the status of the application:

    systemctl status myapp

This can be used to see whether the application is running and to view service information.

---

### Firewall Configuration

The application runs on port `8080`.

Allow traffic to port `8080`:

    sudo firewall-cmd --add-port=8080/tcp

To make the firewall rule permanent:

    sudo firewall-cmd --permanent --add-port=8080/tcp

---

### Testing the Application

Open Firefox and go to:

    http://localhost:8080

If everything is configured correctly, the Node.js application should be accessible through the browser.

---

### Why Use systemd?

Managing an application with systemd provides several benefits:

- The application can start automatically when the system boots.
- The service can be configured to restart if it crashes.
- The application can be managed using standard Linux service commands.
- Systemd can help manage service logging.
- Administrators can use commands such as `systemctl status`, `systemctl start`, and `systemctl stop`.

This means the application behaves like any other managed Linux service.

---

## What I Learned

I learned how to deploy a simple Node.js application on RHEL 10 and manage it using systemd.

I learned how to install Node.js, clone an application from Git, install its dependencies, create a systemd service, and configure the firewall to allow access to the application.

I also learned why managing an application with systemd is useful for automatic startup, recovery, and service management.