# Windows Command Line

## Platform

TryHackMe

## Difficulty

Easy

## Overview

This room introduced basic Windows Command Prompt commands used for system administration, troubleshooting, networking, and process management.

## Command Practised

### System Information

- set - check your path
- ver - determine the OS
- systeminfo - various information about the system such as OS information, system details, processor and memory
- help - provides help information for a specific command
- cls - clears the Command Prompt screen

### Networking

- ipconfig - check ip address, subnet mask and default gateway
- ipconfig /all - we can view our DNS servers and confirm that DHCP is enabled
- ping - checking if we can reach the target and the target reach us
- tracert - traces the network route traversed to reach the target
- nslookup - looks up a host or domain and returns its IP address
- netstat - displays current network connections and listening ports

### File System

- dir - view the child directories
- tree - visually represent the child directories and subdirectories

### Process Management

- tasklist - list the running processes (ex. tasklist /FI "imagename eq notepad.exe")
- taskkill - terminate any task (ex. taskkill /PID 4567)

### System Maintenance

- chkdsk - checks the file system and disk volumes for errors and bad sectors
- driverquery - displays a list of installed device drivers
- sfc /scannow - scans system files for corruption and repairs them if possible

## Key Takeaways

- Windows Command Prompt provides essential tools for system administration and troubleshooting.
- Network commands help diagnose connectivity and DNS issues.
- Process management commands allow monitoring and terminating running applications.
- Built-in Windows utilities can help identify system problems and maintain system integrity.
