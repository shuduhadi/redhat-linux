# Software and Updates Commands

## Check System Registration

    subscription-manager identity

## Register a System

    subscription-manager register

---

## Search for a Package

    dnf search nodejs

## Install a Package

    dnf install nodejs

Automatically answer yes:

    dnf install -y nodejs

---

## Check Available Errata

    dnf updateinfo list

## View Specific Errata

    dnf updateinfo info RHSA-2025:10854

---

## Update the System

    dnf update

## Install Security Updates

    dnf update --security

## Update Important and Critical Security Issues

    dnf update --sec-severity=Important --sec-severity=Critical

---

## Check if a Reboot is Required

    dnf needs-restarting -r

## Reboot the System

    reboot

---

## Red Hat Errata

    RHBA = Bug fixes
    RHEA = Software improvements
    RHSA = Security updates

---

## CVE

    CVE = Common Vulnerabilities and Exposures

CVEs provide a standard, vendor-neutral way of identifying known security vulnerabilities.