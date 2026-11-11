# Active-Directory-Home-Lab


**Windows Server | Active Directory | DNS | Group Policy | Security Auditing | Access Control**

## Project Overview

Built and configured a Windows Server Active Directory environment using VMware Workstation to simulate a small business IT network.

The purpose of this project was to gain hands-on experience with managing users, domain authentication, DNS, Group Policy, security auditing, and file permissions for different departments.

This lab demonstrates practical skills used in IT Support, Help Desk, and Windows Systems Administration.

## Lab Environment

| Component | Configuration |
|---|---|
| Virtualization | VMware Workstation |
| Domain | `ADLAB.LOCAL` |
| Domain Controller | `DC01` |
| Client Workstation | `CLIENT01` |
| Server | Windows Server |
| Technologies | AD DS, DNS, GPO, SMB, NTFS |

## Project Implementation

### 1. Domain Controller and DNS Configuration

- Installed Active Directory Domain Services (AD DS) on Windows Server.
- Promoted `DC01` to a domain controller for `ADLAB.LOCAL`.
- Configured a static IP address and DNS services.
- Configured DNS forwarding to resolve external domain names.

**What I learned:** How domain controllers manage authentication and why DNS is important for Active Directory to function properly.

### 2. Active Directory User and Group Management

- Created organizational units (OUs) for IT, HR, Finance, and Marketing.
- Created domain user accounts and security groups for different departments.
- Organized users into security groups to manage access based on their department.

**What I learned:** How Active Directory makes it easier to manage users and control access through security groups.

### 3. Client Workstation Domain Integration

- Configured `CLIENT01` to use `DC01` as its DNS server.
- Successfully joined `CLIENT01` to the `ADLAB.LOCAL` domain.
- Verified domain authentication using Active Directory credentials.

**What I learned:** How Windows workstations connect to a domain and authenticate users through Active Directory.

### 4. Group Policy and Security Auditing

- Configured Group Policy to audit successful and failed logon attempts.
- Linked the policy to the workstation OU.
- Applied and verified Group Policy using `gpupdate` and `gpresult`.
- Reviewed authentication events using Windows Event Viewer.

**Security Events:**

| Event ID | Description |
|---|---|
| 4624 | Successful logon |
| 4625 | Failed logon |

**What I learned:** How Group Policy and security logs help administrators monitor login activity and troubleshoot authentication problems.

### 5. File Sharing and Permissions for Different Departments

- Created shared folders for IT, HR, Finance, and Marketing.
- Configured SMB file sharing on `DC01`.
- Assigned share and NTFS permissions to security groups for each department.
- Tested folder access from `CLIENT01` using domain user accounts.
- Practiced limiting access based on users' group membership.

**What I learned:** How share and NTFS permissions work together to control who can access files and folders on a network.

## Testing and Troubleshooting

Throughout the lab, I verified configurations and practiced troubleshooting issues involving:

- DNS resolution and domain connectivity.
- Domain authentication and user account access.
- Group Policy application.
- Successful and failed logon auditing.
- Security group membership and shared folder permissions.

These exercises helped me better understand how to identify and resolve common issues in a Windows domain environment.

## Skills Demonstrated

| Windows Administration | Networking and Security |
|---|---|
| Active Directory Domain Services | DNS Configuration |
| User and Group Management | Network Troubleshooting |
| Organizational Units | SMB File Sharing |
| Windows Domain Joining | NTFS and Share Permissions |
| Group Policy Management | Role-Based Access Control |
| Windows Event Viewer | Security Auditing |

## Project Screenshots

Screenshots of the configurations and testing are available in the [screenshots folder](screenshots/).

These screenshots show the Active Directory setup, DNS configuration, security groups, Group Policy, security auditing, and file permissions for different departments.

## Conclusion

This project helped me gain hands-on experience with Windows Server administration, Active Directory, networking, and access management.

By building and troubleshooting a small business IT environment, I strengthened my understanding of how IT administrators manage users, computers, security policies, and access to shared resources.
