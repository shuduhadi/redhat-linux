# Lesson 4 - Command Line Assistant

## Summary

This lesson introduced the RHEL Command Line Assistant (CLI Assistant), an AI-powered feature in Red Hat Enterprise Linux 10 that helps users by answering questions directly from the terminal.

---

## Key Concepts

- RHEL 10 includes an AI-powered Command Line Assistant.
- The CLI Assistant connects to **RHEL Lightspeed**.
- Your RHEL system must be registered to use the AI assistant.
- Registering your system also enables software updates and access to additional Red Hat features.
- Organizations can use a Satellite Server to manage Red Hat software within their own network.

---

## Commands Learned

```bash
c chat "Why should I register RHEL?"
```

---

## Notes

### RHEL Lightspeed

- RHEL 10 includes a built-in AI assistant.
- The Command Line Assistant connects to **RHEL Lightspeed** to answer questions from the terminal.

### System Registration

- Your RHEL system must be **registered** before using the AI assistant.
- An unregistered system cannot access software updates or certain Red Hat features.

### Asking Questions

Use the following command to ask the AI assistant a question:

```bash
c chat "Why should I register RHEL?"
```

### Satellite Server

- A **Satellite Server** allows organizations to mirror Red Hat software inside their own network.
- This provides:
  - Faster access to software and updates.
  - Greater control over software management.
  - Reduced reliance on an internet connection.

---

## What I Learned

I learned that RHEL 10 includes a built-in AI assistant called RHEL Lightspeed, which can answer questions directly from the terminal. I also learned that registering a RHEL system is important because it unlocks updates, additional features, and access to the AI assistant.

---

## Questions

- What other tasks can RHEL Lightspeed help with besides answering questions?
- How do I register a RHEL system?