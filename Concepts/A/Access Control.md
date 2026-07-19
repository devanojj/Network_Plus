#domain/1-0-Networking-Concepts

**==RBAC (Role-Based Access Control)==** 
Access is based on the user's job role (e.g., "Accountant", "Salesperson").

**==DAC (Discretionary Access Control)==** 
The owner of a resource determines who has access. This is the model used in standard file systems like NTFS (Windows) and ext4 (Linux), where you can right-click a file and set permissions.

**==MAC (Mandatory Access Control)==** 
The most restrictive model. Access is determined by a central authority (the operating system) based on security labels. An object has a security level (e.g., "Confidential"), and a user has a clearance level. A user can only access objects at or below their clearance level. Often used in government and military environments.

**==ABAC (Attribute-Based Access Control)==** 
A very flexible model where access is granted based on attributes of the user, the resource, and the environment (e.g., "Allow users from the 'Marketing' department to access the 'Sales-Reports' document between 9 AM and 5 PM from a corporate device.").