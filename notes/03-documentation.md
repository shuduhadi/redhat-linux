# Lesson 3 - Documentation

## Summary

This lesson introduced Linux documentation and how to use manual (man) pages to learn about commands, configuration files, and their syntax.

---

## Key Concepts

- Linux provides built-in documentation through **man pages**.
- Man pages explain how commands work, their options, and required arguments.
- Man pages are also available for configuration files.
- The `man` command has its own manual page.

---

## Commands Learned

```bash
man <command>
man tar
man 5 crontab
```

---

## Notes

### Man Pages

- If you get stuck while using Linux, you can check the documentation instead of searching online.
- **Man pages** provide detailed information about commands, including:
  - What the command does
  - Available options
  - Required arguments
  - Usage examples

### Using the `man` Command

To view the manual page for a command:

```bash
man <command>
```

Example:

```bash
man tar
```

### Searching Within a Man Page

- Press `/` followed by a keyword to search within the manual.
- Press **n** to move to the next search result.
- Press **q** to quit the manual page.

### Man Pages for Configuration Files

Man pages can also explain configuration files.

Example:

```bash
man 5 crontab
```

The **5** specifies that the manual page is for a configuration file or file format.

### Fun Fact

Even the `man` command has its own manual page:

```bash
man man
```

---

## What I Learned

I learned that Linux has built-in documentation that can answer most questions about commands and configuration files. Instead of searching the internet first, I can use man pages to understand how a command works and what options it supports.
