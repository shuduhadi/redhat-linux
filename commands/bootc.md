# Bootc Commands

## Connect to a Bootc Host

    ssh bootchost

---

## Check Bootc Status

    bootc status

---

## Check HTTPD Service

    systemctl status httpd

---

## Check Installed HTTPD Package

    rpm -q httpd

---

## Switch to a New Bootc Image

    bootc switch quay.io/rdcosta/bootc_httpd:2

---

## Reboot the System

    reboot

---

## Test the Application

    http://bootchost.zero-effort.net