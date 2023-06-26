# Access Control (ACL)

## [5 steps to RBAC](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)

1. What is Role Based Access Control (RBAC) and why do we care?
   a) RBAC is the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs. Access is then assigned to each person based strictly on their role assignment. With tight adherence to access requirements established for each role, access management becomes much easier.
   b) Ith an achievable and time-honored approach, we can’t seem to get a handle on access control. We are certainly being pushed in that direction of RBAC, with all of the major standards, including PCI DSS, HIPAA and Gramm-Leach-Bliley all requiring some form of it.

2. Describe a Role/Permission heirarchy that you might implement using RBAC.

a) System Administrator:

- Permissions: Full access to all system resources, including configuration, user management, and sensitive data.

b) Manager:

- Permissions: Can access and modify data within their department.
- Restrictions: Cannot modify system-level configurations or access data from other departments.

c) Team Leader:

- Permissions: Can access and modify data within their team.
- Restrictions: Cannot modify system-level configurations or access data from other teams.

d) Employee:

- Permissions: Can access and modify data relevant to their role.
- Restrictions: Cannot modify system-level configurations or access data from other departments or teams.

e) Guest/Visitor:

- Permissions: Limited access to view certain public information or perform specific actions, such as submitting inquiries or viewing public documents.
- Restrictions: No access to sensitive data or system configurations.

3. What approach might you take to implement RBAC?

   a) Inventory your systems

   Figure out what resources you have for which you need to control access, if you don't already have them listed. Examples would include an email system, customer database, contact management system, major folders on a file server, etc.

   b) Analyze your workforce and create roles

You need to group your workforce members into roles with common access needs. Avoid the temptation to have too many roles defined. Keep them as simple and stratified as possible.

For example, you might have a basic user role, which includes the access any employee would need, such as email and the intranet site. Another role might be a customer service rep, that would have read/write access to the customer database, and a customer database administrator, that would have full control of the customer database.

c) Assign people to roles

Now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.

d) Never make one-off changes

Resist any temptation to make a one-off change for an employee with unusual needs. If you begin doing this, your RBAC system will quickly begin to unravel. Change the roles as required or add new ones when really necessary.

e) Audit

Periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role.

---

## [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

1. If Authentication is “you are who you say you are,” what is Authorization?

Authorization is give the user a permission to do somthing.

2. Name three primary rules defined for RBAC.

   a) Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.

   b) Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.

   c)Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.

3. Describe RBAC to a non-technical friend.
   Imagine you have a big company with many employees, and each employee has their own tasks and responsibilities. RBAC helps ensure that each employee can access only the information and resources they need to do their job effectively. It prevents them from accessing or modifying things that are not relevant to their work.

---

[RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA&ab_channel=Udacity)

1. What Are access rights Associated with? The User? or The Role? Explain.

Associated with the role, Access rights in RBAC are associated with roles, not individual users. Roles are assigned permissions, and users are assigned roles. Users inherit the access rights of the roles they are assigned to.

2. Access Rights, or Authorization, is activated after a user successfully does what?

Authorization, are activated after a user successfully authenticates or verifies their identity.

3. Explain how RBAC might benefit a business.

RBAC benefits businesses by improving security, simplifying access management, increasing efficiency, aiding compliance, and supporting scalability and flexibility.


## [Main Page](../README.md)