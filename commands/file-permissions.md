# File Permissions Commands

## View Permissions

```bash
ls -l
```

## Change File Owner

```bash
chown ricardo foo
```

## Change File Group

```bash
chown :developers foo
```

## Change Owner and Group

```bash
chown ricardo:developers foo
```

## Permission Types

```
r = read
w = write
x = execute
```

## Permission Categories

```
u = user/owner
g = group
o = other
```

## File Permissions

```
r = read the file
w = modify the file
x = execute the file
```

## Directory Permissions

```
r = list directory contents
w = create/delete files
x = access/enter the directory
```

## Example

```
-rwxr-xr--
```

Means:

```
Owner  = rwx
Group  = r-x
Other  = r--
```