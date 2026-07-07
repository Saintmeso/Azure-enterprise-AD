# Project Outcomes & Future Improvements

## Project Overview

This project demonstrates the design and implementation of a centralized enterprise Identity and Access Management (IAM) environment hosted in Microsoft Azure.

The objective was to solve the challenges associated with managing users, permissions, and security across a growing multi-site organization by implementing Active Directory Domain Services, PowerShell automation, Role-Based Access Control (RBAC), shared departmental resources, and centralized Group Policy management.

The completed environment reflects common enterprise administration practices while emphasizing scalability, consistency, and security.

---

# Project Outcomes

The following objectives were successfully completed during the project.

## Enterprise Identity Infrastructure

- Designed a centralized Active Directory environment.
- Organized the directory into Headquarters, Atlanta, Dallas, and Seattle locations.
- Created a scalable Organizational Unit (OU) hierarchy.
- Standardized department organization across every office.

---

## User Provisioning

- Created over 100 enterprise user accounts.
- Standardized usernames and account properties.
- Configured realistic employee attributes including:
  - Department
  - Job Title
  - Company
  - Description
  - Manager

- Automated user provisioning using PowerShell and CSV imports.

---

## Role-Based Access Control

- Created department-specific Security Groups.
- Assigned users to Security Groups based on department and office location.
- Implemented Role-Based Access Control (RBAC).
- Eliminated the need to assign permissions directly to individual users.

---

## Departmental File Sharing

- Designed centralized departmental shared folders.
- Configured Share Permissions.
- Configured NTFS Permissions.
- Protected departmental resources using Security Groups.

---

## Enterprise Security

Implemented Group Policy Objects to standardize enterprise security.

Policies include:

- Password Policy
- Account Lockout Policy
- Screen Lock Policy
- Automatic Windows Updates

---

# Skills Demonstrated

This project demonstrates experience with:

## Microsoft Azure

- Azure Virtual Machines
- Azure Virtual Networking
- Azure Bastion
- Resource Groups

---

## Windows Server Administration

- Windows Server 2022
- Active Directory Domain Services
- Active Directory Users and Computers
- Group Policy Management
- DNS

---

## Identity & Access Management

- Organizational Unit Design
- Security Groups
- Role-Based Access Control (RBAC)
- NTFS Permissions
- Share Permissions

---

## Automation

- PowerShell
- CSV Imports
- Automated User Provisioning

---

# Challenges Encountered

Several challenges were encountered throughout the implementation process.

## Organizational Planning

Designing the Organizational Unit structure required multiple iterations before arriving at a scalable hierarchy capable of supporting multiple office locations and departments.

---

## PowerShell Automation

Developing the provisioning script required troubleshooting CSV formatting, Active Directory paths, and user attribute mapping to ensure accounts were created successfully.

---

## Permission Management

Configuring Share Permissions and NTFS Permissions required careful planning to ensure users only received access through Security Groups while following the Principle of Least Privilege.

---

## Group Policy

Implementing Group Policy required understanding the difference between domain-level policies and policies intended for users or computers, along with selecting configurations that reflected realistic enterprise security requirements.

---

# Future Improvements

If this environment were expanded into a production-ready enterprise deployment, the following enhancements would be considered.

## Identity

- Deploy additional Domain Controllers for redundancy.
- Implement Microsoft Entra ID hybrid identity.
- Configure Azure AD Connect.

---

## Infrastructure

- Deploy Windows 11 domain-joined client workstations.
- Implement Distributed File System (DFS).
- Configure backup and disaster recovery.

---

## Security

- Integrate Microsoft Defender for Cloud.
- Configure Azure Monitor and Log Analytics.
- Implement Multi-Factor Authentication (MFA).
- Enable Privileged Identity Management (PIM).

---

## Automation

- Automate Security Group creation.
- Automate shared folder creation.
- Automate NTFS permission assignment.
- Deploy infrastructure using Infrastructure as Code (IaC).

---

# Final Thoughts

This project demonstrates the design of a scalable enterprise Active Directory environment rather than a basic Active Directory installation.

By combining Microsoft Azure, Active Directory Domain Services, PowerShell automation, Role-Based Access Control, shared resources, and Group Policy, the environment addresses common identity and access management challenges faced by growing organizations.

The project also serves as a foundation for future enhancements, including hybrid identity, cloud security monitoring, and enterprise automation.
