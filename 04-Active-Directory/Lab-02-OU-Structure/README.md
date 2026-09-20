# Lab 02 - Active Directory Organizational Units

## Objectives

In this lab I learned how to:

- Create Organizational Units
- Organize departmental structure
- Create Security Groups
- Create and organize user accounts
- Understand the AGDLP permission model

---

## Environment

- Host OS: Windows 11
- Hypervisor: Oracle VirtualBox 7.2.12
- Server OS: Windows Server 2022
- Domain: bt.local
- Domain Controller: BT-DC01

---

## Organizational Units Created

- Administration
- IT
- HR
- Finance
- Sales
- Servers
- Workstations
- Groups
- Disabled Objects

---

## Final Architecture

## Final Architecture

```text
bt.local
│
├── Administration
│   ├── Users
│   └── Computers
│
├── Finance
│   ├── Users
│   └── Computers
│
├── HR
│   ├── Users
│   └── Computers
│
├── IT
│   ├── Users
│   └── Computers
│
├── Sales
│   ├── Users
│   └── Computers
│
├── Groups
├── Servers
├── Workstations
└── Disabled Objects
```

---

## Users Table

| Name           | Department     | Username  | Group      |
|----------------|----------------|-----------|------------|     
| Alice Brown    | Administration | abrown    | GG_Admin   |
| Michael Wilson | Finance        | mwilson   | GG_Finance |
| Emily Brown    | HR             | ebrown    | GG_HR      |
| John Smith     | IT             | jsmith    | GG_IT      |
| David Miller   | Sales          | dmiller   | GG_Sales   |

---

## AGDLP

Accounts
    ↓
Global Groups
    ↓
Domain Local Groups
    ↓
Permissions

Permissions should be assigned to groups instead of directly to user accounts.

## Why use OU?

Organizational Units allow administrators to:

- Organize Active Directory objects
- Apply Group Policy
- Delegate administration
- Simplify management

---

## Screenshot

./Screenshots/01-Create-OU.png
./Screenshots/02-Created-all-OU.png
./Screenshots/03-Create-users.png

## What I learned

- Default AD containers are different from Organizational Units.
- OUs are primarily used to organize objects and apply Group Policies.
- Security Groups simplify permission management.
- Separating Users and Computers into different OUs prepares the environment for future GPO deployment.
