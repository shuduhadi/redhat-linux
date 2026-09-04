# Lesson 9 - File Permissions

## Summary

This lesson introduced Linux file permissions and how permissions control what users can do with files and directories.

---

## Key Concepts

- Linux uses permissions to control access to files and directories.
- Permissions can be different for the owning user, owning group, and other users.
- The three basic permissions are:
  - `r` = read
  - `w` = write
  - `x` = execute
- Permissions have different meanings depending on whether they are applied to a file or a directory.

---

## Permissions

### Read (`r`)

Read permission allows a user to view the contents of a file or list the contents of a directory.

### Write (`w`)

Write permission allows a user to modify a file or create and delete files inside a directory.

### Execute (`x`)

Execute permission allows a user to run an executable file.

For directories, execute permission allows a user to enter or access the directory.

---

## Directory Permissions

Directory permissions work slightly differently from file permissions.

| Permission | Directory Meaning |
|------------|-------------------|
| `r` | List the contents of the directory |
| `w` | Create and delete files inside the directory |
| `x` | Enter/access the directory |

For example:

- `x` → Change/access the directory
- `rx` → List and access the directory
- `wx` → Create and delete files in the directory
- `rwx` → Full access to the directory

---

## File Permissions

| Permission | File Meaning |
|------------|--------------|
| `r` | Read the contents of the file |
| `w` | Modify the contents of the file |
| `x` | Execute the file |

For example:

- `r` → View the contents
- `w` → Change the contents
- `rx` → Read and execute
- `rwx` → Read, modify, and execute

---

## Permission Categories

Permissions can be set for three categories of users:

### Owner

The user who owns the file.

Example:

```bash
chown ricardo foo
```
This changes the owner of `foo` to `ricardo`.
 
### Group
 
The group that owns the file.
 
Example:
 
```
chown :developers foo
```
 
This changes the group ownership of `foo` to `developers`.
 
### Other
 
Users who are not the owner and are not members of the owning group.
 
## Viewing Permissions
 
Use:
 
```bash
ls -l
```
 
Example output:
 
```bash
-rw-r--r-- 1 ricardo developers 120 Aug 17 10:30 foo
```
 
The first part shows the permissions:
 
```bash
-rw-r--r--
```
 
It can be broken down into:
 
```bash
- rw- r-- r--
```
 
```
  │   │   │
  │   │   └── Other
  │   └────── Group
  └────────── Owner
```
 
The first character indicates the file type:
 
* `-` = regular file
* `d` = directory
## Permission Structure
 
The three permission groups are:
 
```
Owner   Group   Other
 rwx     rwx     rwx
```
 
For example:
 
```
rwxr-xr--
```
 
means:
 
* Owner → `rwx`
* Group → `r-x`
* Other → `r--`
## Changing Ownership
 
Change the owner:
 
```bash
chown ricardo foo
```
 
Change the group:
 
```bash
chown :developers foo
```
 
Change both owner and group:
 
```bash
chown ricardo:developers foo
```
 
## What I Learned
 
I learned that Linux permissions control who can access files and directories and what they are allowed to do.
I learned that `r`, `w`, and `x` have different meanings depending on whether they are applied to a file or directory.
I also learned that permissions are assigned to the owning user, owning group, and other users.
 
