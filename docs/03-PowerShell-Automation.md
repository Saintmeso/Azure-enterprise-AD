# PowerShell Automation

## Business Problem

As Northwind Technologies expanded across four office locations, manually creating employee accounts became increasingly inefficient. Every user account required multiple attributes to be configured, including usernames, departments, job titles, managers, company information, descriptions, and Organizational Unit placement.

Creating more than 100 user accounts manually would be time-consuming, repetitive, and susceptible to human error.

The organization required a standardized provisioning process capable of creating users quickly while ensuring every account followed the same naming conventions and organizational standards.

---

# Solution

To automate user provisioning, I developed a PowerShell script that imports employee information from CSV files and automatically creates Active Directory user accounts.

Instead of manually creating every employee through Active Directory Users and Computers (ADUC), employee information is maintained in Microsoft Excel and exported as CSV files.

Each office location has its own CSV file containing employee information:

- Atlanta
- Dallas
- Seattle

The script imports each CSV and provisions every user with standardized Active Directory attributes.

---

# Why This Approach?

PowerShell automation provides several advantages over manual account creation.

### Consistency

Every employee account follows the same naming convention and organizational standards.

Each user is automatically assigned:

- First Name
- Last Name
- Username
- Department
- Job Title
- Manager
- Company
- Description
- Organizational Unit

---

### Efficiency

Rather than spending several minutes creating each employee manually, dozens of users can be provisioned within seconds.

This significantly reduces administrative overhead during employee onboarding.

---

### Scalability

As additional office locations or departments are introduced, administrators only need to update the CSV file.

The same PowerShell script can then provision the new users without modification.

---

# Implementation

## Step 1 — Create Employee Data

Employee information was first organized in Microsoft Excel before being exported as CSV files.

Separate CSV files were created for:

- Atlanta
- Dallas
- Seattle

Each file contains employee information required to create Active Directory accounts.

<img width="643" height="631" alt="ad pic 3" src="https://github.com/user-attachments/assets/9c31ef9f-7b3d-4f16-a19b-efbb740b4de3" />

---

## Step 2 — Import Active Directory Module

The Active Directory PowerShell module was imported to provide access to Active Directory cmdlets.

--<img width="628" height="525" alt="ad pic 6" src="https://github.com/user-attachments/assets/aaedd4eb-57e3-4024-b884-8409c1c63214" />

---

## Step 3 — Import CSV Data

The script imports employee information directly from the CSV file.

This allows administrators to provision different office locations by changing only the CSV filename.

For example:

AtlantaUsers.csv

↓

DallasUsers.csv

↓

SeattleUsers.csv

The provisioning logic remains exactly the same.

<img width="624" height="421" alt="ad pic 4" src="https://github.com/user-attachments/assets/48840c61-5cd3-4b9c-ae13-0c87d72a5e34" />

---

## Step 4 — User Provisioning

The PowerShell script automatically creates each Active Directory user.

Each account receives standardized properties including:

- Username
- User Principal Name
- Department
- Job Title
- Company
- Description
- Organizational Unit
- Default Password

The script also checks whether a user already exists before creating a new account, preventing duplicate user creation.

<img width="680" height="477" alt="ad pic 5" src="https://github.com/user-attachments/assets/ec99301e-adbc-4d06-9444-583202568cf9" />

---

## Step 5 — Results

After executing the script, all users are automatically created inside their appropriate Organizational Units.

Employee attributes are populated without requiring manual configuration.

Only the CSV file changes between office locations, allowing the same script to provision users for Atlanta, Dallas, and Seattle.

<img width="625" height="528" alt="ad pic 7" src="https://github.com/user-attachments/assets/d2298d1b-ad80-4df5-9a66-831b9aa1b3f7" />

<img width="628" height="532" alt="ad pic 8" src="https://github.com/user-attachments/assets/43681870-beb7-4068-957a-4bf2dd91171c" />

---

# Business Impact

Automating user provisioning significantly reduces the time required to onboard new employees while improving consistency across the enterprise.

Instead of manually configuring every account, administrators can maintain employee information in a spreadsheet and provision entire office locations within seconds.

This approach reduces configuration errors, standardizes account creation, and demonstrates how automation can improve administrative efficiency in enterprise Active Directory environments.
