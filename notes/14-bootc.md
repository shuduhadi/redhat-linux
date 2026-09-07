# Lesson 14 - Using Image Mode with Bootc

## Summary

This lesson introduced bootc and Image Mode for RHEL. Instead of building and configuring a server piece by piece, the entire operating system and its applications are packaged into a complete image that acts as a blueprint for the system.

---

## Key Concepts

- Bootc uses complete system images instead of building a server piece by piece.
- An image contains the operating system, applications, and configuration needed for the system.
- When changes are needed, a new image can be built with the updated packages or configuration.
- The server can then be switched to the new image and rebooted.
- If something goes wrong, the system can roll back to a previous image.
- Image-based systems make upgrades more predictable and consistent.
- Bootc helps administrators know exactly what version of the operating system and applications are running.

---

## Commands Learned

    ssh bootchost
    bootc status
    systemctl status httpd
    rpm -q httpd
    bootc switch quay.io/rdcosta/bootc_httpd:2
    reboot

---

## Notes

### What is Bootc?

Bootc is a way of running RHEL using an image-based approach.

Instead of installing and configuring every part of a server separately, you use a complete image that acts as a blueprint for the system.

The image can contain:

- The operating system
- Applications
- Configuration
- Packages

This makes it easier to reproduce the same system consistently.

---

### Updating the System

With an image-based system, updates and upgrades are made by creating a new image.

The server can then be switched to the new image.

The general process is:

1. Build a new image with the required changes.
2. Point the server to the new image.
3. Reboot the server.
4. The system starts using the new image.

This makes upgrades more predictable because the entire system is updated as a single unit.

---

### Rolling Back

If an updated image causes a problem, the system can be rolled back to the previous image.

This makes it easier to recover from failed upgrades without manually rebuilding the server.

---

### Connecting to the Bootc Host

The demo uses a RHEL 10 server called `bootchost`.

Connect to the server using SSH:

    ssh bootchost

---

### Checking Bootc Status

To view information about the current image and bootc system:

    bootc status

---

### Checking the HTTPD Service

The demo server already has the Apache HTTP server installed and running.

Check its status:

    systemctl status httpd

Check whether the HTTPD package is installed:

    rpm -q httpd

---

### Testing the Web Server

The application can be accessed through a web browser:

    http://bootchost.zero-effort.net

The demo initially shows:

    OS and app version: 1

This demonstrates serving static content from an image-based RHEL system.

---

### Switching to a New Image

To switch the server to version 2 of the image:

    bootc switch quay.io/rdcosta/bootc_httpd:2

The system then:

- Downloads the new image.
- Incorporates the new image filesystem into the bootc host.
- Prepares the system to boot using the new image.

After switching images, reboot the system:

    reboot

After the reboot, the server is now running:

    OS and app version: 2

---

## What I Learned

I learned that bootc allows RHEL systems to be managed using complete system images instead of configuring each server individually.

I learned that upgrades can be made by switching to a new image and rebooting, while previous images can be used for rollback if something goes wrong.

This approach makes server upgrades more predictable and helps ensure that systems run exactly the versions and configurations that were intended.

---

## Questions

- How are bootc images created?
- How does bootc decide which image to boot?
