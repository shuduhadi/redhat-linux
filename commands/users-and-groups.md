# Users and Groups Commands

## View Local Users

```bash
cat /etc/passwd
```

## View Password/Shadow Information

```bash
cat /etc/shadow
```

## Create a User

```bash
useradd allison
```

## Set a User's Password

```bash
passwd allison
```

## Modify a User

```bash
usermod -s /bin/zsh allison
```

## Delete a User

```bash
userdel allison
```

## Delete a User and Their Home Directory

```bash
userdel -r allison
```

## Lock a User Account

```bash
passwd -l allison
```

## Unlock a User Account

```bash
passwd -u allison
```

## Create a Group

```bash
groupadd developers
```

## Modify a Group

```bash
groupmod developers
```

## Delete a Group

```bash
groupdel developers
```

## Check User Information (UID, Groups)

```bash
id allison
```

## Check a User's Group Memberships

```bash
groups allison
```

## Add a User to the wheel Group

```bash
usermod -aG wheel curtis
```

## Find Files Owned by a Specific User ID

```bash
find -uid 1001 2>/dev/null
```

## Start a Root Shell

```bash
sudo -i
```

## Switch to Root User

```bash
su -
```