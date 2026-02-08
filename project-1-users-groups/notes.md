Project 1: Users, Groups & Permissions (Ubuntu Server)
Overview
This project demonstrates practical Linux system administration skills by configuring users, groups, and file permissions on an Ubuntu Server. The goal was to implement secure, group-based access control and verify permissions through hands-on testing.
________________________________________
Objective
•	Create and manage Linux users and groups
•	Configure directory ownership and permissions
•	Apply the principle of least privilege
•	Test and validate access control
________________________________________
 Environment
Operating System: Ubuntu Server
•	Access Method: Local Linux Terminal
•	Privileges: Root / sudo
________________________________________
User and Group Management
Groups Created
•	staff
•	it
Users Created
•	john
•	sarah
•	noc
Group Membership
•	john → staff
•	sarah → staff
•	noc → no staff access
Group membership was verified using standard Linux commands.
________________________________________
Shared Directory Configuration
•	Directory: /srv/shared
•	Owner: root
•	Group: staff
Permissions Applied
•	Full access for owner and staff group
•	No access for others # noc -staff user  is denied
This setup ensures that only authorized staff users can access the shared directory.
________________________________________
Access Testing
Access was tested by switching between users and attempting to access the shared directory.
User	Group	Result
john	staff	- Access allowed
sarah	staff	- Access allowed
noc	none	    - Permission denied
This confirms that group-based permission control is working as expected.
________________________________________
Commands Used
•	useradd
•	groupadd
•	usermod
•	chmod
•	chown
•	id
•	getent
•	su
Key learnings
- Linux permission model: owner / group / others
- Least privilege and access control testing
