# Departmental Shared Folders

## Business Problem

As organizations expand, employees across multiple departments require access to shared files and resources. Without a structured file-sharing system, business data can become disorganized, difficult to locate, and vulnerable to unauthorized access.

For Northwind Technologies, each department manages information that should only be accessible to authorized employees. For example, Human Resources stores employee records, Finance manages payroll and budgeting documents, and Engineering maintains technical documentation.

The organization required a centralized file-sharing solution that allowed departments to collaborate while ensuring sensitive information remained protected.

---

# Solution

To address this challenge, departmental shared folders were created for each office location within the enterprise environment.

Each location contains dedicated folders for every department, allowing resources to remain organized while supporting Role-Based Access Control (RBAC).

Folder access is controlled through Active Directory Security Groups rather than individual user accounts, ensuring permissions remain scalable and easy to manage.

---

# Folder Structure

A centralized **Shares** directory was created on the Domain Controller.

```
C:\Shares
│
├── Headquarters
│   ├── Accounting
│   ├── Engineering
│   ├── Finance
│   ├── HR
│   ├── IT
│   ├── Marketing
│   ├── Operations
│   ├── Public
│   └── Sales
│
├── Atlanta
│   ├── Accounting
│   ├── Engineering
│   ├── Finance
│   ├── HR
│   ├── IT
│   ├── Marketing
│   ├── Operations
│   ├── Public
│   └── Sales
│
├── Dallas
│   ├── Accounting
│   ├── Engineering
│   ├── Finance
│   ├── HR
│   ├── IT
│   ├── Marketing
│   ├── Operations
│   ├── Public
│   └── Sales
│
└── Seattle
    ├── Accounting
    ├── Engineering
    ├── Finance
    ├── HR
    ├── IT
    ├── Marketing
    ├── Operations
    ├── Public
    └── Sales
```

> **Insert screenshot of the Shares directory**

<img width="768" height="575" alt="ad pic 12" src="https://github.com/user-attachments/assets/01a3e485-44f9-436f-96fb-e7f22b727828" />

# Access Control Strategy

Each departmental folder is protected using Role-Based Access Control (RBAC).

Rather than assigning permissions directly to users, access is granted through Active Directory Security Groups.

For example:

| Department Folder | Security Group |
|-------------------|----------------|
| Atlanta Finance | Atlanta Finance |
| Atlanta HR | Atlanta HR |
| Atlanta IT | Atlanta IT |
| Atlanta Sales | Atlanta Sales |

This ensures that employees automatically receive the correct permissions through group membership.

<img width="775" height="556" alt="ad pic 11" src="https://github.com/user-attachments/assets/66f07ee2-6128-43a1-a953-03d5c0b29853" />

---

# Share Permissions

Each departmental folder was configured as a shared network resource.

Share permissions were configured to:

- Allow authorized department Security Groups access.
- Restrict unauthorized users from accessing departmental resources.
- Provide Domain Administrators with full administrative control.

This creates a secure and centralized file-sharing environment for the organization.

<img width="353" height="469" alt="ad pic 13" src="https://github.com/user-attachments/assets/3cb30a06-b001-4d9c-8efd-65378be51336" />

---

# NTFS Permissions

NTFS permissions provide the primary layer of access control for departmental resources.

Each folder was configured to:

- Remove unnecessary inherited permissions.
- Grant Modify permissions to the appropriate department Security Group.
- Retain Full Control for Domain Administrators and the SYSTEM account.

This approach follows the Principle of Least Privilege by ensuring users only have access to resources required for their job responsibilities.

<img width="748" height="503" alt="ad pic 14" src="https://github.com/user-attachments/assets/26efb177-bdfa-4701-9bcf-236381238c1a" />

---

# Why This Approach?

Using departmental shared folders combined with Security Groups provides several operational benefits.

### Improved Organization

Each office maintains its own departmental file structure, making resources easier to locate and manage.

---

### Simplified Administration

Administrators no longer manage permissions for individual users.

Instead, access is controlled by modifying Security Group membership.

---

### Improved Security

Sensitive business information remains accessible only to authorized departments.

For example:

- Finance employees cannot access HR documents.
- Sales employees cannot access Finance records.
- Engineering employees cannot access HR files.

---

### Scalability

As new employees join the organization, administrators simply add them to the appropriate Security Group.

No changes to folder permissions are required.

---

# Business Impact

Implementing departmental shared folders provides Northwind Technologies with a secure and scalable file-sharing solution.

By combining centralized file storage with Role-Based Access Control, the organization reduces administrative overhead, improves collaboration within departments, and protects sensitive business information from unauthorized access.

This design supports future organizational growth while maintaining a consistent and manageable permission model across every office location.
