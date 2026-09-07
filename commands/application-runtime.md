# Application Runtime Commands

## Install Node.js

    sudo dnf install -y nodejs

---

## Clone the Application

    git clone https://gitlab.com/rgdacosta/nodejs_rhel10.git

---

## Enter the Application Directory

    cd nodejs_rhel10/

---

## List Application Files

    ls

---

## View package.json

    cat package.json

---

## Install Node.js Dependencies

    npm install

---

## Copy the systemd Service File

    sudo cp myapp.service /etc/systemd/system/

---

## Reload systemd

    sudo systemctl daemon-reload

---

## Start and Enable the Application

    sudo systemctl enable --now myapp

---

## Check Application Status

    systemctl status myapp

---

## Allow Port 8080

    sudo firewall-cmd --add-port=8080/tcp

---

## Make Port 8080 Permanent

    sudo firewall-cmd --permanent --add-port=8080/tcp

---

## Test the Application

    http://localhost:8080