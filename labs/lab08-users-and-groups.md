# Lab 8 - Organizing Local Users and Groups

## Objective

Practice creating and managing local Linux users and groups.

## Tasks Completed

- Created a test user.
- Set a password for the user.
- Checked the user's information.
- Created a group.
- Added the user to the group.
- Checked the user's groups.
- Locked and unlocked the account.
- Deleted the test user and their home directory.

## Commands Used

```bash
useradd testuser
passwd testuser

id testuser

groupadd testgroup

usermod -aG testgroup testuser

groups testuser

passwd -l testuser
passwd -u testuser

userdel -r testuser
```
## Practice
- Created a local test user.
- Created a test group.
- Added the user to the group.
- Used id and groups to check the user's information.
- Practiced locking and unlocking the account.
- Removed the test user and home directory.


## Outcome
I successfully practiced the basic commands used to manage local users and groups in Linux. I also learned how groups can be used to organize users and manage access.