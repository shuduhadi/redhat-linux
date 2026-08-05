# Lesson 7 - Editing Files with Vim

## Summary

This lesson introduced Vim, a lightweight text editor included with Linux. It covered the different modes in Vim and basic commands for editing, saving, and quitting files.

---

## Key Concepts

- Vim is included in every RHEL installation.
- It is a fast and lightweight text editor.
- Vim is commonly used to edit configuration files.
- Vim has different modes, each with a specific purpose.

---

## Commands Learned

```bash
vim filename.txt
vimtutor
```

---

## Notes

### What is Vim?

- Vim is a text editor included in every Linux installation.
- It is fast, lightweight, and commonly used to edit configuration files.

### Vim Modes

#### Normal Mode
- The default mode when Vim opens.
- Used for navigation and running commands.

#### Insert Mode
- Used to type and edit text.
- Press `i` to enter Insert Mode.
- Press `Esc` to return to Normal Mode.

#### Command Mode
- Used for saving, quitting, searching, and other commands.
- Enter Command Mode by pressing `:` while in Normal Mode.

### Useful Vim Commands

| Command | Purpose |
|---------|---------|
| `i` | Enter Insert Mode |
| `Esc` | Return to Normal Mode |
| `:q!` | Quit without saving |
| `yy` | Copy (yank) the current line |
| `p` | Paste the copied line |
| `10p` | Paste the copied line 10 times |
| `u` | Undo the last change |
| `Ctrl + r` | Redo the last undone change |

### Learning Vim

- Run `vimtutor` in the terminal to complete the built-in Vim tutorial.

---

## What I Learned

I learned that Vim uses different modes for editing text and running commands. Although it is different from most text editors, it is a powerful tool for editing files directly from the terminal.
