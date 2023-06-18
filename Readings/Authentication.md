# Authentication

[Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

1. Explain to a non-technical friend how you would safely hash and store a password.

   When you register for an online service or make an account, the website or app takes your password and uses a special algorithm to turn it into a random sequence of characters. This process is called hashing, and it makes it really hard for anyone to guess or uncover your actual password.

2. What is Bcrypt?

   Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.

3. Why might you use something like Bcrypt?

   It extremely resistant to brute force attacks.

---

[Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

1. What is Basic Authentication?
   HTTP authentication.

2. What properties are necessary in the header of a Basic
   Auth request?
   A request contains a header field in the form of Authorization: Basic credentials.

3. How are username:password in Basic Auth encoded?
   credentials is the Base64 encoding of ID and password joined by a single colon :.

---

[OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

1. Define the authentication process to a non-technical recruiter.

   Authentication is the process of verifying that an individual, entity or website is whom it claims to be

2. How should your error messaging respond (both HTTP and HTML)? Why?

   a) HTTP Response: When responding to authentication errors at the HTTP level, use appropriate status codes. For example:

   1. 401 Unauthorized: This status code indicates that the user is not authenticated or lacks valid credentials.

   2. 403 Forbidden: This status code indicates that the server understood the request, but the user is not allowed to access the requested resource.
   3. 400 Bad Request: This status code can be used for general authentication errors.

   b) HTML Response: In the HTML response, display a generic error message without providing specific details about the nature of the error. Avoid indicating whether the user ID or password was incorrect, if the account exists or not, or any other specific error details.
