# Linux Fundamentals part 3

## Platform

TryHackMe

## Difficulty

Easy

## Overview

## Command Used

### Python3 -m http.server

```bash
python3 -m http.server
```

This command starts a simple HTTP server that can be used to share files over a network.
They can be downloaded using commands like "curl" and "wget"

### Wget

```bash
wget http://10.113.159.114:8000/.flag.txt
```

For example, this command downloads a file named .flag.txt from a remote web server and saves it locally.

### Systemctl

```bash
systemctl start apache2
```

This command allows us to interact with the systemd process/daemon. It takes the following formatting:
systemctl [option] [service] We can do five options with systemctl:

- start
- stop
- enable
- disable
- status

### Reading Logs

```bash
tryhackme@linux3:/var$ cd log
tryhackme@linux3:/var/log$ cd apache2
tryhackme@linux3:/var/log/apache2$ ls
access.log    error.log    error.log.2.gz
access.log.1  error.log.1  other_vhosts_access.log
tryhackme@linux3:/var/log/apache2$ cat access.log.1
10.9.232.111 - - [04/May/2021:18:18:16 +0000] "GET /catsanddogs.jpg HTTP/1.1" 200 51395 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36"
```

While using this commands i could get into access.log.1 log and read that: address of user who visited the site is 10.9.232.111, and user accessed catsanddogs.jpg file.

## Other command practiced

- nano
- scp
- curl
- ps
- ps aux
- top
- kill
- fg

## Key Takeaways

- Linux services can be managed through systemctl.
- Log files provide valuable information about user activity.
- Simple HTTP servers can be used to transfer files between systems.
- Process monitoring is important for system administration and security investigations.

## SOC Perspective

- Unexpected use of "python3 -m http.server" could indicate unauthorized file sharing or data exfiltration.
- Apache access logs can help identify suspicious activity such as repeated requests to administrative pages.
- Process monitoring tools like top can help detect abnormal resource usage caused by malware or misconfigured applications.
- Downloading files with tools such as wget should be investigated when the source or file purpose is unknown.
