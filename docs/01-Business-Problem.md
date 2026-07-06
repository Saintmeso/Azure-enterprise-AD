# Business Problem

## Overview

As organizations grow, managing employee identities, access permissions, and security policies becomes increasingly complex. What may initially work for a small business quickly becomes difficult to manage as additional employees, departments, and office locations are introduced.

Northwind Technologies has expanded from a single office into a multi-site organization with Headquarters, Atlanta, Dallas, and Seattle offices. As the company continued to grow, identity management processes became inconsistent, user provisioning was performed manually, and access to shared resources was difficult to manage securely.

Without a centralized identity management solution, the organization faced increasing administrative overhead, inconsistent security practices, and a greater risk of unauthorized access to sensitive business information.

---

# Business Challenges

The following challenges were identified during the organization's growth.

## 1. Inconsistent Identity Management

Employee accounts were created manually without a standardized organizational structure.

As additional offices and departments were introduced, it became increasingly difficult to maintain consistency across users, departments, and administrative processes.

This resulted in:

- Inconsistent user provisioning
- Difficult user administration
- Increased onboarding time
- Greater potential for configuration errors

---

## 2. Inefficient Access Management

Permissions were difficult to manage as the organization expanded.

Without Role-Based Access Control (RBAC), administrators would eventually need to assign permissions directly to individual users, making access management increasingly difficult to maintain.

This introduced several risks:

- Excessive administrative effort
- Permission inconsistencies
- Unauthorized access to sensitive departmental information
- Difficult employee onboarding and offboarding

---

## 3. Lack of Centralized Security Policies

As additional employees joined the organization, maintaining consistent workstation security became increasingly challenging.

Without centralized management, systems could develop inconsistent password requirements, security configurations, and update schedules.

Examples include:

- Weak password policies
- Missing account lockout protection
- Inconsistent Windows Update configurations
- Workstations left unsecured after periods of inactivity

---

# Project Objective

The objective of this project was to design and implement a centralized enterprise Identity and Access Management (IAM) environment capable of supporting a growing multi-site organization.

The environment was built using Microsoft Azure and Active Directory Domain Services while following common enterprise administration practices.

The solution focuses on improving administrative efficiency, strengthening security, and creating a scalable infrastructure capable of supporting future organizational growth.

---

# Proposed Solution

To address these challenges, a centralized enterprise infrastructure was designed and implemented with the following objectives:

- Deploy Active Directory Domain Services in Microsoft Azure.
- Design a scalable Organizational Unit (OU) structure for multiple office locations.
- Standardize user provisioning through PowerShell automation.
- Implement Role-Based Access Control (RBAC) using Active Directory Security Groups.
- Secure departmental resources using NTFS and Share Permissions.
- Enforce centralized security policies using Group Policy Objects (GPOs).

---

# Business Value

By implementing centralized identity management, the organization benefits from:

- Standardized employee onboarding and account management.
- Improved security through centralized policy enforcement.
- Simplified permission management using Security Groups.
- Reduced administrative effort through PowerShell automation.
- A scalable infrastructure capable of supporting continued organizational growth.
