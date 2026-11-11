# Active-Directory-Home-Lab
Project Overview: 
This project demonstrates my hands-on experience configuring and managing a Windows Server Active Directory environment using VMware Workstation.
I built this lab to strengthen my understanding of Windows Server administration, networking, identity and access management, Group Policy, security auditing, and file-sharing permissions.

The goal was to simulate a small business IT environment where employees belong to different departments and receive access to network resources based on their assigned roles.

Lab Environment:

Virtualization Platform: VMware Workstation

Domain: ADLAB.LOCAL

Domain Controller: DC01

Client Workstation: CLIENT01

Technologies Used:

Windows Server

Active Directory Domain Services (AD DS)

DNS

Group Policy Management

Active Directory Users and Computers (ADUC)

Windows Event Viewer

SMB File Sharing

NTFS and Share Permissions

Project Objectives

Deploy and configure a Windows Server domain controller.

Configure DNS and establish domain connectivity.

Join a Windows client workstation to the domain.

Create organizational units, user accounts, and security groups.

Manage department access using security groups.

Configure Group Policy for successful and failed logon auditing.

Review Windows Security Event Logs to verify auditing.

Configure departments shared folders with appropriate permissions.

Test authorized and unauthorized access to network resources.

Project Implementation

The following sections document the configuration, verification, troubleshooting, and testing performed throughout the lab.

1. Windows Server and Domain Controller Configuration

Configured a Windows Server virtual machine named DC01 and installed Active Directory Domain Services.

Promoted DC01 to a domain controller for the ADLAB.LOCAL domain.

Configured a static IP address and DNS services to provide reliable domain connectivity and name resolution.

2. Active Directory Organization

Created organizational units to organize users and departments.

Configured security groups based on departments to manage access permissions through group membership rather than assigning permissions individually.

3. Client Domain Integration

Configured CLIENT01 to use DC01 for DNS resolution and successfully joined the workstation to ADLAB.LOCAL.

Verified connectivity and domain Group Policy processing.

4. Group Policy and Security Auditing

Configured Group Policy to audit successful and failed logon events on the domain-joined workstation.

Verified policy application using gpupdate and gpresult.

Reviewed Windows Event Viewer Security Logs and identified:

Event ID 4624 — Successful logon

Event ID 4625 — Failed logon

5. Department File Sharing and Access Control

Configured shared folders for the departments of IT, HR, Finance, and Marketing.

Assigned share and NTFS permissions to security groups that are organized by departments.

Tested network folder access from CLIENT01 to evaluate role-based access restrictions and the principle of least privilege.

Skills Demonstrated

Windows Server Administration

Active Directory Domain Services

DNS Configuration and Troubleshooting

Domain Joining

User and Group Management

Organizational Unit Management

Group Policy Configuration

Windows Security Event Log Analysis

SMB File Sharing

NTFS and Share Permissions

Role-Based Access Control

Network Troubleshooting

Project Documentation

Screenshots documenting the configurations and testing are available in the screenshots directory.

Conclusion

This lab provided practical experience administering a Windows domain environment and troubleshooting authentication, networking, Group Policy, and resource access.

It strengthened my understanding of how IT administrators manage users, workstations, permissions, and security policies in a business environment.
