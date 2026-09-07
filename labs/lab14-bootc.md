# Lab 14 - Using Image Mode with Bootc

## Objective

Understand how bootc uses complete system images to manage RHEL systems and practice switching a system to a newer image.

---

## Tasks Completed

- Connected to a RHEL 10 bootc host using SSH.
- Checked the bootc system status.
- Checked the HTTPD service.
- Verified that HTTPD was installed.
- Viewed the application running on the bootc host.
- Switched the host from image version 1 to image version 2.
- Rebooted the system.
- Verified that the new image was running.

---

## Commands Used

Connect to the host:

    ssh bootchost

Check bootc status:

    bootc status

Check HTTPD:

    systemctl status httpd

Check the installed package:

    rpm -q httpd

Switch to image version 2:

    bootc switch quay.io/rdcosta/bootc_httpd:2

Reboot:

    reboot

---

## Practice

I used SSH to connect to the bootc host and checked the current system using `bootc status`.

I checked that the Apache HTTP server was running and verified that the HTTPD package was installed.

I then switched the system from image version 1 to image version 2 and rebooted the server.

After the reboot, the system was running the updated OS and application version.

---

## Outcome

I learned how image-based RHEL systems can be updated by switching to a new image instead of manually updating individual components.

I also learned how this approach makes upgrades more predictable and provides the ability to roll back to a previous image if something goes wrong.