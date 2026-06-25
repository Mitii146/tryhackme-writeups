# Active Directory Basics

## Platform

TryHackMe

## Difficulty

Easy

## Overview

This room introduced the fundamentals of Active Directory (AD), including domains, users, groups, Organizational Units (OUs), Group Policy Objects (GPOs), and authentication concepts used in enterprise Windows environments.

## Key Concepts

### Active Directory Domain Service

This service acts as a catalogue that holds the information of all of the "objects" that exist on your network. Amongst the many objects supported by we have users, groups, machines, printers, shares and many others. AD helps administrators manage users, computers, and resources across an organization.

### Using Group Policy Management

GPOs are simply a collection of settings that can be applied to Organizational Units (OUs). GPOs can contain policies aimed at either users or computers, allowing you to set a baseline on specific machines and identities

### Organizational Units (OUs)

Organizational Units are containers used to organize users, groups, and computers within a domain. They help administrators apply policies and delegate management.

### Authentication

Active Directory uses authentication protocols such as Kerberos to verify the identity of users and computers within a domain.

### Trees, Forests and Trusts

A Tree is a collection of domains sharing a common namespace. Multiple trees form a Forest, which is the top-level structure in Active Directory. Trusts allow users from one domain to access resources in another domain.

## Key Takeaways

- Active Directory centralizes management of users, computers, and resources in enterprise environments.
- Organizational Units (OUs) help organize objects and simplify administration.
- Group Policy Objects (GPOs) allow administrators to enforce security and configuration settings across multiple systems.
- Authentication is a core function of AD and commonly relies on Kerberos.
- Forests, Trees, and Trusts enable communication and resource sharing between domains.

## SOC Perspective

- Active Directory is a common target for attackers because it manages authentication and authorization across the organization.
- Monitoring authentication events can help detect brute-force attacks and unauthorized access attempts.
- Misconfigured Group Policy Objects (GPOs) may introduce security weaknesses across multiple systems.
- Compromising a privileged AD account can allow attackers to move laterally through the network.
