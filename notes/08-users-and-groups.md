# Lesson 8 - Organizing Local Users and Groups

## Summary

This lesson introduced local users and groups in Linux, where user information is stored, and how users and groups can be created, modified, locked, and deleted.

---

## Key Concepts

- User and group information is stored in `/etc`.
- `/etc/passwd` stores information about local users.
- Password information is stored separately in `/etc/shadow`.
- `sudo` allows trusted users to perform administrative tasks.
- Groups are used to organize users and manage access.
- The `wheel` group is the default administrative group in RHEL.

---

## Commands Learned

```bash
cat /etc/passwd
useradd
passwd
usermod
userdel
groupadd
groupmod
groupdel
id
groups
sudo
su
```
# Notes

## Local Users

Local users are typically used in:

* Standalone servers
* Test machines
* Small environments where access is managed locally

For larger environments, organizations can use centralized identity management systems such as Identity Management (IdM) or Active Directory.

## `/etc`

The `/etc` directory contains configuration data for the system.
It also contains files related to local users and groups.

### `/etc/passwd`

The `/etc/passwd` file contains information about local users.
It does not store user passwords.

To view the local users:

```
cat /etc/passwd
```

### `/etc/shadow`

User password information is stored in:

```
/etc/shadow
```

This file is more restricted because it contains sensitive password-related information.

## sudo

`sudo` means superuser do.
It allows trusted users to run commands with administrative privileges without having to log in directly as the root user.

## Creating a User

The `useradd` command creates a new user.

Example:

```
useradd allison
```

A password can then be created using:

```
passwd allison
```

## Modifying a User

The `usermod` command is used to change user settings.

For example, to change a user's login shell:

```
usermod -s /bin/zsh allison
```

This changes Allison's login shell to Zsh.

## Deleting a User

The `userdel` command removes a user.

```
userdel allison
```

To remove the user and their home directory:

```
userdel -r allison
```

## Locking and Unlocking Users

A user account can be locked using:

```
passwd -l allison
```

The account can be unlocked using:

```
passwd -u allison
```

## Groups

Groups allow multiple users to be organized together.
They are useful for managing access and permissions for multiple users.

Create a group:

```
groupadd developers
```

Modify a group:

```
groupmod
```

Delete a group:

```
groupdel developers
```

## Checking User Information

The `id` command displays information about a user, including their user ID and group memberships.

```
id allison
```

The `groups` command shows which groups a user belongs to.

```
groups allison
```

## The wheel Group

The `wheel` group is the default administrative group in RHEL.
Users who are members of this group can be given permission to perform administrative tasks using `sudo`.

Add a user to the `wheel` group:

```
usermod -aG wheel curtis
```

Check the user's information:

```
id curtis
```

Check the user's groups:

```
groups curtis
```

## Finding Files Owned by a User

The `find` command can be used to find files owned by a specific user ID.

For example:

```
find -uid 1001 2>/dev/null
```

Here:

* `find` searches for files and directories.
* `-uid 1001` searches for files owned by user ID `1001`.
* `2>/dev/null` hides error messages.

## Root Shell

A root shell can be started using:

```
sudo -i
```

This gives the user a root shell if they have the required administrative privileges.

Another way to switch users is:

```
su -
```

This can be used to switch to the root user when the appropriate permissions and credentials are available.

## What I Learned

I learned how Linux manages local users and groups and where their information is stored. I learned how to create, modify, lock, and delete user accounts and how to create and manage groups.

I also learned about the `wheel` group and how it can be used to give users administrative access through `sudo`.

## Questions

* What is the difference between `sudo` and `su`?
* What information is stored in `/etc/passwd`?
* Why is `/etc/shadow` protected?
* What is the purpose of the `wheel` group?
* What is the difference between local users and centralized identity management?

