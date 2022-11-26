# Active Directory Basics

## Windows Domains

- created to overcome scaling difficulties
- Windows Domain = group of users and computers under administration of one organization
	- centralize basic administration into a single repository - Active Directory (AD)
	- Domain Controller (DC) = server that runs AD services
- centralize identity management
- central configuration of security policies

### A Real-World Example

- you've probably used AD when signing into an organization's device with credentials created by that org

### Welcome to THM Inc.

- Configure domain "THM.local"
- RDP THM\Administrator
	- domain = THM
	- user = Administrator

## Active Directory

- Active Directory Domain Service (AD DS) - service that holds all information about objects in a domain
	- Users - type of domain object known as security principals
		- can act upon other objects in a domain
		- may be users or services
	- Machines - type of domain object, also considered security principals
		- are granted limited local admin rights on only themselves
		- passwords are created randomly with 120 characters
		- machine account is computer's name followed by dollar sign (e.g. *Computer-Name$*)
	- Security Groups - used for managing privileges in bulk
		- can include users, machines, other groups, objects
		- some important groups are listed below:
| Security Group | Description |
| -------------- | ----------- |
| Domain Admins | administrators of the entire domain |
| Server Operators | Administrators of DCs only |
| Backup Operators | may access any file regardless of file permissions; meant for backing up data |
| Account Operators | may create or modify domain accounts |
| Domain Users | all user accounts in domain |
| Domain Computers | all computers in domain |
| Domain Controllers | all DCs in domain |

### Active Directory Users and Computers

- on Windows Server open start menu and enter "Active Directory Users and Computers" to configure AD objects 
- objects are organized with OUs (Organizational Units) which classify sets of objects based on their policies
	- each user may be part of one OU at a time
	- OUs typically follow the structure of business units
- domains come with some default containers:
	- builtin - default groups
	- computers - default location for machines added to the domain
	- domain controllers - default OU for DCs
	- users - default users and groups
	- managed service accounts - accounts used by domain services

### Security Groups vs OUs

- OUs are for policy application and users can only be part of one OU at a time
- Security groups are for granting permissions to resources

## Managing Users in AD

- do the THM exercises and play around with a ~~really slow~~ normal Windows Server

## Managing Computers in AD

- 3 types of devices/"computers":
	1. Workstations - users PCs; most common
	2. Servers - provide services among themselves
	3. Domain Controllers - allow management of domain
- create separate OUs for different device types

## Group Policies

- 

