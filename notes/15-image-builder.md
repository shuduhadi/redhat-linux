# Lesson 15 - Insights Image Builder

## Summary

This lesson introduced golden images and the different image builder tools available for creating consistent RHEL systems. Image builders allow you to create customized RHEL images that can be deployed across servers or virtual machines.

---

## Key Concepts

- A **golden image** is a ready-to-use snapshot of an operating system.
- Golden images provide a clean and consistent starting point for servers and virtual machines.
- Image builders allow you to customize an operating system image before deploying it.
- **Insights Image Builder** is a hosted service available through the Red Hat Hybrid Cloud Console.
- **RHEL Image Builder** is installed directly on a RHEL system.
- Both image builders provide similar core functionality.
- Images can start with a minimal installation and then be customized with packages, users, scripts, security settings, and other configuration.
- Images can be created for different environments, including virtual machines.

---

## Commands Learned

No specific Linux commands were introduced in this lesson.

The lesson focused mainly on using the Red Hat Hybrid Cloud Console and Insights Image Builder.

---

## Notes

### Golden Images

A **golden image** is a ready-to-use snapshot of an operating system.

It provides a clean and consistent starting point for deploying servers or virtual machines.

Using golden images provides several benefits:

- Deployments are faster.
- Deployments are more predictable.
- Systems can follow the same standards.
- Less manual configuration is required.
- Configuration mistakes can be reduced.

---

### Insights Image Builder

**Insights Image Builder** is a hosted image building service from Red Hat.

It is available through the **Red Hat Hybrid Cloud Console**.

One of the main benefits is that you do not need to install or maintain separate image-building infrastructure.

Everything can be managed through a web interface.

Benefits include:

- Image creation from the cloud.
- No additional build infrastructure to maintain.
- Ability to preview new features.
- Integration with other Red Hat Insights tools.
- Centralized image management.
- Access through a web browser from different locations.

---

### RHEL Image Builder

**RHEL Image Builder** is a feature that can be installed directly on a RHEL system.

It provides:

- A command-line interface (CLI).
- A graphical interface (GUI).
- Integration with the RHEL web console.

---

### Image Builder Features

Insights Image Builder and RHEL Image Builder share many of the same core features.

By default, an image can start with a **minimal installation**, containing only the essential components needed for the system.

Additional configuration can then be added.

Examples include:

- Additional software packages.
- Custom scripts.
- User accounts.
- Time zones.
- Hostnames.
- Firewall services and ports.
- systemd services.
- Security and compliance profiles.

This makes it possible to create systems that are consistent, secure, and customized for specific requirements.

---

### Creating an Image with Insights Image Builder

The general process demonstrated in the lesson was:

1. Open a web browser.
2. Navigate to:

    https://console.redhat.com

3. Select **Insights for RHEL**.
4. Expand **Inventory**.
5. Select **Images**.
6. Create a new image blueprint for RHEL 10.
7. Select the architecture.
8. Choose a virtualization guest image.
9. Configure the image settings.
10. Add any required packages and users.
11. Configure networking, firewall, and system services.
12. Give the blueprint a name.
13. Create the blueprint.
14. Generate the image.

---

### Image Configuration

The demonstrated image configuration included:

- **Operating System:** RHEL 10
- **Architecture:** x86_64
- **Image Type:** General virtualization guest image
- **Format:** `.qcow2`
- **Registration:** Enabled
- **Advanced capabilities:** Enabled
- **Partitioning:** Recommended partitioning
- **Repeatable builds:** Disabled to provide more control
- **Custom packages:** Additional packages such as OpenJDK
- **User accounts:** Custom users can be added
- **Timezone:** Configurable
- **Hostname:** Configurable
- **Kernel:** Standard kernel package
- **Firewall:** Services and ports can be selected
- **systemd:** Services can be enabled

---

### QCOW2 Images

The image can be generated in the `.qcow2` format.

QCOW2 images are commonly used with virtual machines.

Once the image has been generated, it can be downloaded and used to create virtual machines.

---

## What I Learned

I learned that golden images provide a consistent starting point for deploying servers and virtual machines.

I also learned about Insights Image Builder and RHEL Image Builder and how they can be used to create customized RHEL images.

I learned that an image can be customized with packages, users, networking, firewall rules, systemd services, and security settings before it is deployed.
