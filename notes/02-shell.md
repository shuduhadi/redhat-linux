# Lesson 2 - Introduction to the Shell

## Summary

This lesson introduced the Linux shell, how commands are structured, and useful shell features like tab completion.

---

## Key Concepts

- The shell allows you to work on a Linux system remotely.
- The default shell in RHEL is **Bash (Bourne Again Shell)**.
- The shell's purpose is to interpret and execute the commands entered by the user.
- Linux commands follow a basic structure: **command → options → arguments**.

---

## Commands Learned

```bash
du -sh /home/rgdacosta
```

---

## Notes

### What is the Shell?

- The shell provides the flexibility to work on a server remotely.
- Commands are run inside a shell.
- The default shell in RHEL is **Bash**.
- The shell interprets and executes the commands entered by the user.

### Basic Command Structure

A Linux command is made up of three parts:

```text
command [options] [arguments]
```

- **Command** – The action you want to perform.
- **Options** – Modify how the command runs. Options usually begin with a single dash (`-`) or double dash (`--`).
- **Arguments** – The file, directory, or object the command should work on.

Example:

```bash
du -sh /home/rgdacosta
```

- `du` → Command
- `-sh` → Options (`-s` for summary and `-h` for human-readable output)
- `/home/rgdacosta` → Argument (the directory to check)

### Tab Completion

- Press **Tab** to automatically complete commands, file names, or directories.
- If there are multiple possible matches, press **Tab** twice to display the available options.
- If nothing happens when you press Tab, type more characters until the name is unique enough to complete.

Examples:

- Auto-complete a directory:

```bash
cd /usr/sh<Tab>
```

- View available Podman subcommands:

```bash
podman<Tab><Tab>
```

### Documentation

- Always check a command's documentation to understand the available options and required arguments.

---

## What I Learned

I learned that the shell is the interface used to interact with Linux through commands. I also learned how Linux commands are structured using commands, options, and arguments, and how tab completion can make working in the terminal faster and more efficient.

---

## Questions

- What are some other useful Bash features besides tab completion?
- What is the difference between a shell and a terminal?
```