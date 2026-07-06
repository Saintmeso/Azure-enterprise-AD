# Enterprise Organizational Unit (OU) Design

## Business Problem

As organizations expand across multiple offices and departments, managing users in a single Active Directory container quickly becomes difficult. Administrative tasks become harder to delegate, security policies become inconsistent, and locating users, computers, or groups becomes increasingly inefficient.

Northwind Technologies required a directory structure capable of supporting multiple office locations while remaining scalable as additional employees, departments, and resources were introduced.

---

# Solution

To support future growth, I designed a hierarchical Organizational Unit (OU) structure that separates resources by **office location**, **resource type**, and **department**.

Instead of storing all objects in a single location, every office contains dedicated Organizational Units for:

- Users
- Groups
- Computers

Each Users OU is further organized into business departments, creating a logical structure that mirrors how the company operates.

This approach simplifies administration, supports future delegation, and provides a foundation for applying department or location-specific Group Policy Objects (GPOs).

---

# Enterprise Directory Structure

```
northwind.local
│
├── Headquarters
│   ├── Users
│   ├── Groups
│   └── Computers
│
├── Atlanta
│   ├── Users
│   ├── Groups
│   └── Computers
│
├── Dallas
│   ├── Users
│   ├── Groups
│   └── Computers
│
├── Seattle
│   ├── Users
│   ├── Groups
│   └── Computers
│
├── Servers
├── Workstations
└── Disabled Accounts
```



---

# Department Structure

Within each office, the Users Organizational Unit is divided into departments that represent the company's business operations.

Departments include:

- Executive / Local Management
- Information Technology (IT)
- Help Desk
- Human Resources
- Finance
- Accounting
- Marketing
- Sales
- Engineering
- Operations

Each department contains employees assigned to realistic job titles and reporting structures.

<img width="233" height="680" alt="ad pic 2" src="https://github.com/user-attachments/assets/b21ec51a-fdc7-48d3-80ff-500d2c88103d" />

Every user account includes:

- Department
- Job Title
- Manager
- Company
- Description

This creates a realistic enterprise directory that reflects how employees are organized within a business.

<img width="774" height="539" alt="ad pic 1" src="https://github.com/user-attachments/assets/903ac468-4446-4794-9439-ccf9de921be3" />

---

# Why This Design?

Rather than creating one large Users Organizational Unit, separating resources by location and department provides several advantages.

### Simplified Administration

Administrators can quickly locate users based on office location and department without searching the entire directory.

---

### Scalability

Additional office locations or departments can be added without restructuring the existing environment.

---

### Delegation

Administrative responsibilities can be delegated to specific Organizational Units without granting unnecessary permissions across the entire domain.

For example:

- Help Desk administrators could manage password resets for one office.
- HR administrators could manage employee accounts.
- Future branch administrators could manage only their assigned location.

---

### Group Policy Flexibility

The Organizational Unit structure provides a logical target for future Group Policy deployment.

Examples include:

- Department-specific security policies
- Location-specific desktop configurations
- Software deployment by department
- Device restrictions for Finance and HR

---

# Design Decisions

Several design decisions were made while planning the directory structure.

### Multi-Site Organization

The environment was separated into Headquarters, Atlanta, Dallas, and Seattle to simulate a geographically distributed organization.

This allows each location to manage its own users, computers, and security groups while maintaining centralized authentication through Active Directory.

---

### Dedicated Resource Organizational Units

Each location contains separate Organizational Units for:

- Users
- Groups
- Computers

Separating these resources improves organization and follows common enterprise Active Directory design practices.

---

### Disabled Accounts Organizational Unit

Rather than deleting employee accounts after termination, disabled accounts are moved into a dedicated Organizational Unit.

This preserves account history while preventing unauthorized access and reflects common enterprise lifecycle management practices.

---

# Business Impact

A well-designed Organizational Unit hierarchy serves as the foundation for every other component within the Active Directory environment.

By organizing resources according to business function rather than convenience, the directory becomes easier to manage, supports future growth, enables delegated administration, and provides a scalable framework for centralized identity and access management.
