# Access Control (ACL)

## Questions & Answers

[5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

1. What is Role Based Access Control (RBAC) and why do we care?
  It is a way to get certain users a 'role' that gives them access to certain
  parts of the application. We care because it is a way to control what users
  can do.
2. Describer a Role/Permission heirarchy that you might implement using RBAC.
  A user can have the role 'admin' which gives them access to everything,
  'editor' might give them a chance to edit things, and 'viewer' can only read.
3. What approach might you take to implement RBAC?
  The way we did it in lab was using this scenario of having seperate sql tables
  for practitioners, and patients. We would have 'roles' for each of role of the
  user and then the practitioners would have CRUD access to their records but only
  read access for the patients forms. The patients would only have read access to
  their own records.

---

[wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

1. If Authentication is "you are who you say you are," what is Authorization?
  And you are allowed to do what you are allowed to do.
2. Name three primary rules defined for RBAC.
    - Role assignment
    - Role authorization
    - Permission authorization
3. Describe RBAC to a non-technical friend.
  It is a way to control what people can do in an application. Certain people
  who are in charge of the app can do once thing, while their users can do another!

---

[RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

1. What are access rights Associated with? The User? Explain.
  These are the permissions that a user has once their role has been assigned.
2. Access Rights, or Authorization, is activated after a user successfully does what?
  After they have been authenticated.
3. Explain how RBAC might benefit a business.
  It helps with how the business controls who can do what in the application.
