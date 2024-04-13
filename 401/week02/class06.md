# Authentication

Reading assignment 'Read 06'

## Questions & Answers

[Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

1. Explain to a non-technical friend how you would safely hash and store a password.
You would put in the password you would like to use, and the server would immediately
run a formula of sorts that will turn your password into a combinations of characters
that are not easily reversible. Then the server will store that combination of characters.
When you log in, the server will run the same formula on the password you entered
and compare it to the stored combination of characters. If they match, you are allowed
in.
2. What is Bcrypt?
It is a Node.js library that allows you to hash passwords.
3. Why might you use something like Bcrypt?
It is a secure way to store passwords. It is a one way hash that is not easily reversible.

---

[Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

1. What is Basic Authentication?
It is a way to send a username and password in an HTTP request.
2. What properties are necessary in the header of a Basic Authentication request?
The `Authorization` header is necessary.
3. How are `username:password` in Basic Auth encoded?
They are encoded in base64.

---

[OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

1. Define the authentication process to a non-technical recruiter.
It is a process that runs a function on the very request that is made to the server.
It will check if a user is truly who they say they are.
2. How should you error messaging respond (both HTTP and HTML)? Why?
You should not give away too much information. You should respond with a 401 status
code and a generic message.
3. Bookmark this link also and consider OWASP fundamentals any time you interact
with authentication. Applications developed with security in mind from inception
have fewer vulnerabilities throughout their lifecycle.
