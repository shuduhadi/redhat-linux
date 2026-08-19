# Lesson 10 - Managing Software and Updates

## Summary

This lesson introduced how RHEL systems are registered, how software packages are searched for and installed, and how Red Hat manages bug fixes, improvements, and security updates through errata.

---

## Key Concepts

- RHEL systems need to be registered to access Red Hat content and updates.
- `subscription-manager` is used to check registration and register a system.
- RHEL uses `dnf` to search for, install, and update software packages.
- Satellite can provide Red Hat content to multiple servers from within an organization's network.
- Red Hat publishes updates through different types of errata.
- Security advisories are linked to CVEs.
- Security updates can be filtered by severity.
- Some updates may require the system to be restarted.

---

## Commands Learned

    subscription-manager identity
    subscription-manager register
    dnf search nodejs
    dnf install nodejs
    dnf install -y nodejs
    dnf updateinfo list
    dnf updateinfo info RHSA-2025:10854
    dnf update
    dnf update --security
    dnf update --sec-severity=Important --sec-severity=Critical
    dnf needs-restarting -r
    reboot

---

## Notes

### System Registration

Before managing RHEL software and updates, you should check whether the system is registered.

    subscription-manager identity

If the system is not registered:

    subscription-manager register

### Satellite

If an organization has several RHEL servers that do not have direct access to the Red Hat Content Delivery Network (CDN), it can use a Satellite server.

Satellite acts as a proxy for Red Hat content.

The Satellite server:

- Connects to the internet.
- Downloads Red Hat content from the CDN.
- Stores the content locally.
- Makes the content available to systems inside the organization's network.

This allows organizations to manage software and updates centrally.

### Managing Packages with DNF

`dnf` is used to manage software packages in RHEL.

#### Searching for Packages

    dnf search nodejs

#### Installing Packages

    dnf install nodejs

The `-y` option automatically answers yes to the confirmation prompt:

    dnf install -y nodejs

### Red Hat Errata

Red Hat publishes different types of advisories called **errata**.

#### RHBA - Red Hat Bug Advisory

- Provides bug fixes.
- Fixes problems found in existing software.

#### RHEA - Red Hat Enhancement Advisory

- Provides improvements and enhancements to existing software.

#### RHSA - Red Hat Security Advisory

- Provides security updates.
- Addresses security vulnerabilities.

### CVEs

**CVE** stands for **Common Vulnerabilities and Exposures**.

CVEs provide a vendor-neutral way of identifying known security vulnerabilities.

When a package is affected by a vulnerability:

- It can be assigned a CVE ID.
- The vulnerability can receive a severity score.
- The score helps indicate how serious the vulnerability is.

### Checking Errata

To list available errata:

    dnf updateinfo list

To view information about a specific advisory:

    dnf updateinfo info RHSA-2025:10854

### Updating the System

Update the entire system:

    dnf update

Update security-related packages:

    dnf update --security

Limit security updates to important and critical severity:

    dnf update --sec-severity=Important --sec-severity=Critical

### Checking if a Reboot is Needed

    dnf needs-restarting -r

If a reboot is required:

    reboot

---

## What I Learned

I learned how to check whether a RHEL system is registered and how to register it using `subscription-manager`.

I also learned how to use `dnf` to search for and install packages and how Red Hat uses errata to provide bug fixes, software improvements, and security updates.

I learned about CVEs and how they are used to identify security vulnerabilities and understand their severity.

---

## Questions

- What is the difference between RHBA, RHEA, and RHSA?
- Why would an organization use Satellite?
- What is a CVE?
- Why might a system need to be rebooted after an update?