# Linux Fundamentals Part 2

## Platform

TryHackMe

## Difficulty

Easy

## Overview

## Command Used

### SSH

```bash
ssh user@IP
```

Used to remotely connect to a Linux system

### SU

```bash
su username
```

Used to switch to other user

### CHMOD

```bash
chmod 777 filename
```

Used to change file access, where 777 is full access (read, write, execute) for owner groups others
For example:

- Read (r) = 4
- Write (w) = 2
- Execute (x) = 1

- Owner (rwx) = 4 + 2 + 1 = 7
- Group (rwx) = 4 + 2 + 1 = 7
- Others (rwx) = 4 + 2 + 1 = 7

We can change it for example:

```bash
chmod 750 filename
```

- Owner: full access
- Group: read + execute
- Others: no access

## Other command practiced

- ls, ls -a, ls -lh
- man
- touch
- mkdir
- rm
- cp
- mv
- file
- Basic Linux directories:
  /etc, /var, /root, /tmp

## Key Takeaways

In this room I have learned:

- SSH is commonly used for remote administration and can be an entry point for attackers if misconfigured.
- File permissions in Linux are critical for system security and access control.
- Understanding commands like chmod helps in identifying misconfigured systems and privilege issues.
- The Linux filesystem structure (/etc, /var, /root) is important when investigating system behavior and logs.

## SOC Perspective

In a real-world scenario, I would pay attention to:

- unauthorized SSH access attempts
- unusual user switching (su usage)
- incorrect file permissions (777 as a security risk)
