# Active-Directory-Home-Lab


**Windows Server | Active Directory | DNS | Group Policy | Security Auditing | Access Control | Ubuntu Linux**

## Project Overview

Built and configured a Windows Server Active Directory environment using VMware Workstation to simulate a small business IT network.

The purpose of this project was to gain hands-on experience with managing users, domain authentication, DNS, Group Policy, security auditing, and file permissions across different departments.

This lab demonstrates practical skills used in IT Support, Help Desk, and Windows Systems Administration.

## Lab Environment

| Component | Configuration |
|---|---|
| Virtualization | VMware Workstation |
| Domain | `ADLAB.LOCAL` |
| Domain Controller | `DC01` |
| Client Workstation | `CLIENT01` |
| Server | Windows Server |
| Linux Server | Ubuntu Server |
| Technologies | AD DS, DNS, GPO, SMB, NTFS, Linux |

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

### 6. Ubuntu Linux Server Integration

- Installed and configured an Ubuntu Server virtual machine using VMware Workstation.

- Configured network connectivity between Ubuntu Server and the Windows Server environment.

- Verified connectivity to DC01.

- Successfully joined Ubuntu Server to the ADLAB.LOCAL domain.

**What I learned:** How Linux systems can integrate with a Windows Active Directory environment and use centralized identity management.


## Testing and Troubleshooting

Throughout the lab, I verified configurations and troubleshot issues involving DNS, domain authentication, Group Policy, and network permissions.

### DNS Resolution Troubleshooting

During the initial configuration, external DNS lookups were unsuccessful.

- Investigated DNS resolution using `nslookup`.
- Configured DNS forwarding on `DC01`.
- Verified that external domain names could be resolved successfully.

### Domain Connectivity and Authentication

- Verified network connectivity between `DC01` and `CLIENT01`.
- Configured the client to use the domain controller for DNS.
- Troubleshot domain authentication and successfully signed in using domain credentials.

### Group Policy and Security Auditing

- Applied Group Policy updates using `gpupdate`.
- Verified policy application using `gpresult`.
- Reviewed successful and failed logon events in Windows Event Viewer.

### File Share Access Testing

- Tested access to shared folders using domain user accounts.
- Verified that security group membership controlled access to network resources.
- Confirmed that users without the required permissions were restricted from accessing protected folders.


### Ubuntu Linux Connectivity

- Troubleshot initial network connectivity issues between Ubuntu Server and the Windows Server environment.
- Verified connectivity after bringing the domain controller online.
- Successfully integrated Ubuntu Server into the Active Directory domain.

These exercises strengthened my ability to identify and resolve common issues in a Windows and Linux network environment.




## Skills Demonstrated

| **Systems Administration** | **Networking and Security** |
|---|---|
| Active Directory Domain Services | DNS Configuration |
| Windows Server Administration | Network Troubleshooting |
| Ubuntu Linux Server | Domain Authentication |
| User and Group Management | SMB File Sharing |
| Organizational Units | NTFS and Share Permissions |
| Windows Domain Joining | Role-Based Access Control |
| Linux Domain Integration | Security Auditing |
| Group Policy Management | Windows Event Viewer |


## Project Screenshots

Screenshots documenting the Windows Server configurations, Active Directory management, DNS, Group Policy, auditing, and file permissions are available in the repository. 

[screenshots folder](screenshots/).

### Ubuntu Linux Server Screenshots

These screenshots document Ubuntu Server configuration, network connectivity, and integration with the `ADLAB.LOCAL` Active Directory domain.








## Conclusion

This project provided hands-on experience with Windows Server administration, Active Directory, Linux integration, networking, and access management.

By building and troubleshooting a small business IT environment, I strengthened my understanding of how administrators manage users, computers, authentication, security policies, and network resources across Windows and Linux systems.

This lab serves as a foundation for my continued learning in IT Support, Systems Administration, and Identity and Access Management.
