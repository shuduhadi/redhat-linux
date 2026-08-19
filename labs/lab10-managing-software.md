# Lab 10 - Managing Software and Updates

## Objective

Practice checking system registration, searching for packages, installing software, viewing errata, and checking whether the system needs updates or a reboot.

---

## Tasks Completed

- Checked whether the RHEL system was registered.
- Learned how to register a RHEL system.
- Searched for a software package.
- Installed a software package.
- Viewed available errata.
- Viewed information about a security advisory.
- Learned how to install security updates.
- Checked whether the system requires a reboot.

---

## Commands Used

Check registration:

    subscription-manager identity

Search for a package:

    dnf search nodejs

Install a package:

    dnf install nodejs

View available errata:

    dnf updateinfo list

View a specific advisory:

    dnf updateinfo info RHSA-2025:10854

Check whether a reboot is required:

    dnf needs-restarting -r

---

## Practice

I practiced using `dnf` to search for packages and learned how packages can be installed and updated.

I also learned how Red Hat uses RHBA, RHEA, and RHSA advisories to provide bug fixes, improvements, and security updates.

I learned how CVEs are used to identify vulnerabilities and how security updates can be filtered by severity.

---

## Outcome

I learned how RHEL software and updates are managed using `subscription-manager` and `dnf`. I also learned how organizations can use Satellite to manage Red Hat content across multiple systems.