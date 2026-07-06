# Role-Based Access Control (RBAC)

## Business Problem

As organizations grow, managing permissions for individual employees becomes increasingly difficult. Assigning permissions directly to user accounts creates unnecessary administrative overhead and makes it difficult to maintain consistent access controls across departments.

For example, if a Finance employee transfers to Marketing, an administrator would need to manually remove and assign multiple permissions. As the number of employees increases, this process becomes inefficient and increases the risk of excessive or incorrect permissions.

Northwind Technologies required a scalable access management model capable of supporting multiple office locations while ensuring employees only had access to the resources required for their role.

---

# Solution

To address this challenge, Role-Based Access Control (RBAC) was implemented using Active Directory Security Groups.

Instead of assigning permissions directly to users, permissions are assigned to Security Groups that represent specific departments and office locations.

Users receive access by becoming members of the appropriate Security Group.

This approach separates user management from permission management, making administrative tasks significantly easier.

---

# Why Role-Based Access Control?

Implementing RBAC provides several advantages over assigning permissions directly to individual users.

### Simplified Administration

Administrators only manage group membership instead of configuring permissions for every employee individually.

When a new employee joins the company, they simply become a member of the appropriate department group.

---

### Improved Security

Permissions follow the Principle of Least Privilege.

Employees receive access only to the resources required for their department and job responsibilities.

---

### Scalability

As additional employees, departments, or office locations are introduced, existing Security Groups can continue to be used without redesigning the permission structure.

---

### Easier Employee Lifecycle Management

Employee onboarding, department transfers, promotions, and offboarding become significantly easier.

Rather than modifying folder permissions, administrators simply update Security Group membership.

---

# Security Group Design

Each office location contains dedicated Security Groups for every department.

Examples include:

- Atlanta Accounting
- Atlanta Finance
- Atlanta HR
- Atlanta IT
- Atlanta Marketing
- Atlanta Sales
- Atlanta Engineering
- Atlanta Operations

The same structure is repeated for:

- Headquarters
- Dallas
- Seattle

This standardized naming convention improves consistency throughout the Active Directory environment.

<img width="955" height="778" alt="ad pic 9" src="https://github.com/user-attachments/assets/5ff3c787-8bc7-4c2a-8823-aaa4676cdac8" />

---

# Group Membership

Each employee was assigned to the Security Group associated with their office location and department.

For example:

| User | Department | Security Group |
|-------|------------|----------------|
| Ryan Mitchell | Management | Atlanta Local Management |
| Ashley Foster | IT | Atlanta IT |
| Lauren Brooks | Human Resources | Atlanta HR |
| Eric Simmons | Finance | Atlanta Finance |

This allows permissions to be managed through group membership rather than individual user accounts.

<img width="390" height="440" alt="ad pic 10" src="https://github.com/user-attachments/assets/0b9516d9-457c-478c-abb1-457aaf6846aa" />

---

# How RBAC Supports Shared Resources

The Security Groups created in Active Directory are later used to secure departmental shared folders.

Rather than granting folder permissions directly to employees, permissions are assigned to the department Security Groups.

For example:

| Shared Folder | Authorized Group |
|---------------|------------------|
| Atlanta Finance | Atlanta Finance |
| Atlanta HR | Atlanta HR |
| Atlanta IT | Atlanta IT |
| Atlanta Sales | Atlanta Sales |

This creates a consistent permission model throughout the environment while reducing administrative effort.

---

# Business Impact

Implementing Role-Based Access Control transformed permission management from a user-based model into a role-based model.

Instead of manually configuring permissions for every employee, administrators only manage Security Group membership.

This approach:

- Reduces administrative overhead
- Simplifies employee onboarding and offboarding
- Supports organizational growth
- Improves security through the Principle of Least Privilege
- Provides a scalable permission model suitable for enterprise environments
