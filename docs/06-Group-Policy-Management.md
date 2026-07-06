# Group Policy Management

## Business Problem

As organizations grow, maintaining consistent security configurations across every system becomes increasingly difficult. Without centralized management, password requirements, account lockout settings, workstation security, and update policies can vary between devices, increasing administrative overhead and exposing the organization to unnecessary security risks.

Northwind Technologies required a centralized solution capable of enforcing standardized security policies across the enterprise while reducing manual configuration and ensuring every system complied with organizational security standards.

---

# Solution

To address these challenges, Group Policy Objects (GPOs) were implemented to centrally manage security settings across the Active Directory environment.

Rather than configuring each workstation individually, administrators can define policies once and automatically apply them throughout the domain.

The following Group Policy Objects were implemented:

- Password Policy
- Account Lockout Policy
- Screen Lock Policy
- Automatic Windows Updates

These policies establish a consistent security baseline across the enterprise.

---

# Why Group Policy?

Group Policy is one of the most powerful administrative features available within Active Directory.

Instead of relying on manual configuration, administrators can centrally manage security settings for every domain-joined system.

This approach provides:

- Consistent security configurations
- Reduced administrative effort
- Centralized management
- Improved compliance
- Simplified future administration

---

# Implemented Policies

## Password Policy

A domain-wide password policy was implemented to improve account security.

Configuration includes:

- Minimum password length
- Password complexity requirements
- Password expiration
- Password history

These settings reduce the likelihood of weak or reused passwords.

<img width="595" height="430" alt="ad pic 15" src="https://github.com/user-attachments/assets/64d0a0b5-30bf-4ea6-bd3f-5363ef4fae64" />
---

## Account Lockout Policy

To help protect against brute-force password attacks, an Account Lockout Policy was configured.

Configuration includes:

- Account lockout threshold
- Lockout duration
- Reset lockout counter

This helps prevent repeated password guessing attempts while allowing legitimate users to regain access after the configured lockout period.

<img width="543" height="392" alt="ad pic 16" src="https://github.com/user-attachments/assets/8783181e-c5c8-4dea-a9ef-9e2391597a7a" />

---


---

## Automatic Windows Updates

Automatic Windows Updates were configured through Group Policy to help maintain system security and reduce exposure to known vulnerabilities.

Configuration includes:

- Automatic download of updates
- Scheduled installation
- Active hours configuration to prevent unexpected restarts during business hours

Centralized update management helps ensure systems remain secure without requiring manual intervention.

<img width="543" height="508" alt="ad pic 17" src="https://github.com/user-attachments/assets/0ffc8095-68e6-4388-9b60-6d05ce20628a" />

---

# Why These Policies?

The selected policies were chosen because they address common security risks found in enterprise environments.

| Policy | Business Benefit |
|----------|------------------|
| Password Policy | Improves account security by enforcing stronger passwords. |
| Account Lockout | Reduces the risk of brute-force password attacks. |
| Windows Updates | Ensures systems remain protected against known vulnerabilities. |

Together, these policies establish a standardized security baseline across the organization.

---

# Business Impact

Implementing Group Policy allows Northwind Technologies to centrally manage enterprise security without manually configuring individual systems.

By standardizing password requirements, account protection, workstation security, and update management, the organization reduces administrative effort while improving overall security and consistency.

As the organization grows, additional policies can be deployed using the existing Group Policy infrastructure, providing a scalable foundation for future security initiatives.
