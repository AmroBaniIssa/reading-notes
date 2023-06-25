What is Role Based Access Control (RBAC) and why do we care?

  Role-Based Access Control (RBAC) is a security model that defines and manages access control based on roles assigned to individual users within an organization. In RBAC, permissions are associated with specific roles, and users are assigned one or more roles based on their responsibilities and job functions. This approach provides a structured and efficient way to control access to resources in a system.

Describe a Role/Permission heirarchy that you might implement using RBAC.
  Regular users can READ.
  Writers can READ and CREATE.
  Editors can READ, CREATE, and UPDATE.
  Administrators can READ, CREATE, UPDATE, and DELETE.

What approach might you take to implement RBAC?
  1. Inventory your systems
       Figure out what resources you have for which you need to control access
  2. Analyze your workforce and create roles
       You need to group your workforce members into roles with common access needs
  3. Assign people to roles
       Now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.     
  4. Never make one-off changes
       Resist any temptation to make a one-off change for an employee with unusual needs
  5. Audit
       Periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role. 


If Authentication is “you are who you say you are,” what is Authorization?

   Authorization, in the context of security, refers to the process of granting or denying access rights and permissions to authenticated users or entities based on their identity, role, or other attributes. While authentication verifies the identity of a user, authorization determines what actions or resources that user is allowed to access or perform within a system.
 
   In simpler terms, if authentication is about confirming "you are who you say you are," then authorization is about answering the question "what are you allowed to do?"

Name three primary rules defined for RBAC.
   - Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
   - Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.
   - Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.

Describe RBAC to a non-technical friend.
   Imagine you have a big company with different departments and many employees. Each employee has different roles and responsibilities,  RBAC, which stands for Role-Based Access Control, is like a system that helps manage who has access to what within the company's computer systems.

   Think of it as having different levels of access or permissions. Just like how in the real world, certain employees have access to specific areas or information based on their job roles, RBAC works the same way for computer systems.

