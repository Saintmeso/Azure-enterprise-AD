# Project Timeline

This timeline outlines the overall implementation process used to design and deploy the enterprise Identity & Access Management (IAM) environment.

Rather than building every component simultaneously, the environment was developed in logical phases. Each phase builds upon the previous one, mirroring how an enterprise infrastructure would typically be implemented.

---

# Phase 1 — Infrastructure Planning

Before deploying Active Directory, the enterprise environment was planned to support future organizational growth.

Objectives:

- Define the business requirements.
- Identify office locations.
- Design the enterprise directory structure.
- Plan user lifecycle and access management.

**Outcome**

A scalable enterprise design capable of supporting multiple office locations and departments.

---

# Phase 2 — Active Directory Deployment

A Windows Server 2022 virtual machine was deployed in Microsoft Azure and promoted to a Domain Controller.

Major Tasks:

- Install Active Directory Domain Services (AD DS)
- Configure DNS
- Create the northwind.local domain

**Outcome**

A centralized identity platform for the organization.

---

# Phase 3 — Enterprise Directory Design

The Active Directory environment was organized to reflect the company's organizational structure.

Major Tasks:

- Headquarters
- Atlanta
- Dallas
- Seattle

Each location includes:

- Users
- Groups
- Computers

Departmental Organizational Units were created for:

- Executive / Local Management
- IT
- Help Desk
- HR
- Finance
- Accounting
- Marketing
- Sales
- Engineering
- Operations

**Outcome**

A scalable Organizational Unit (OU) hierarchy that supports future growth and simplifies administration.

---

# Phase 4 — Enterprise User Provisioning

Employee accounts were created using a combination of manual provisioning and PowerShell automation.

Major Tasks:

- Create realistic employee accounts
- Standardize usernames
- Assign departments
- Assign job titles
- Assign managers
- Import users using PowerShell and CSV files

**Outcome**

More than 100 standardized Active Directory user accounts were successfully provisioned.

---

# Phase 5 — Identity & Access Management

Role-Based Access Control (RBAC) was implemented using Active Directory Security Groups.

Major Tasks:

- Create department Security Groups
- Assign users to groups
- Organize permissions based on department and office location

**Outcome**

Permissions can now be managed through Security Group membership instead of individual user accounts.

---

# Phase 6 — Departmental File Services

Shared departmental folders were created for every office location.

Major Tasks:

- Create centralized file shares
- Configure Share Permissions
- Configure NTFS Permissions
- Protect departmental resources using Security Groups

**Outcome**

Departments can securely collaborate while maintaining access restrictions based on organizational roles.

---

# Phase 7 — Enterprise Security

Group Policy Objects (GPOs) were implemented to establish a standardized security baseline.

Policies implemented include:

- Password Policy
- Account Lockout Policy
- Screen Lock Policy
- Automatic Windows Updates

**Outcome**

Security settings can now be centrally managed across the Active Directory environment.

---

# Project Summary

The completed environment demonstrates the design and implementation of a centralized enterprise Identity & Access Management (IAM) solution hosted in Microsoft Azure.

The project successfully integrates:

- Microsoft Azure
- Windows Server 2022
- Active Directory Domain Services
- Organizational Unit Design
- PowerShell Automation
- Role-Based Access Control (RBAC)
- Departmental Shared Folders
- Group Policy

Together, these components provide a scalable foundation for managing users, permissions, and security across a growing multi-site organization.
