Securing Passwords:

Explain to a non-technical friend how you would safely hash and store a password.
    Imagine you have a password that you want to store securely. Instead of storing the password itself, we use a special function called a hash function. A hash function takes an input (in this case, the password) and produces a fixed-size string of characters, which is the hash.
    So, when a user creates an account and sets a password, we take that password and run it through the hash function to generate a hash. We store the hash in our database, but we don't store the actual password.
    Now, when the user tries to log in, we take the entered password, run it through the same hash function, and generate a hash from it. We then compare this newly generated hash with the hash we have stored in the database. If the two hashes match, it means the entered password is correct without ever having to store or expose the actual password.
    hashing and storing a password safely involves using a one-way hash function to convert the password into an irreversible hash value. We store the hash in the database, not the password itself, and during login attempts, we compare the generated hash with the stored hash to authenticate the user. This approach provides an added layer of security to protect user passwords.

What is Bcrypt?

    Bcrypt is a widely used hashing algorithm that is specifically designed for password hashing and is considered highly secure. It is an adaptive hash function, which means it can be configured to consume more computational resources as hardware capabilities increase over time, making it resistant to brute-force attacks.

 Bcrypt incorporates several techniques to ensure password security. Here are a few key features:

    Salt: Bcrypt automatically generates a random salt value for each password hash. The salt is then included as part of the resulting hash. Salting prevents attackers from using precomputed tables (rainbow tables) to crack passwords in bulk.

    Work Factor: Bcrypt allows you to define a "cost factor" that determines the number of iterations the algorithm performs. Increasing the work factor exponentially increases the time required to hash a password. This feature makes the hashing process slow and computationally expensive, making it difficult for attackers to crack passwords through brute-force or dictionary attacks.

    Hash Output: The hash output of Bcrypt includes the salt, work factor, and the actual hashed password. This ensures that all the necessary information to verify a password is contained within the hash itself.


Why might you use something like Bcrypt?
    By combining the techniques above, Bcrypt provides a strong defense against password cracking attempts. It ensures that even if an attacker gains access to the hashed passwords, it would take an impractical amount of time and computational power to reverse-engineer the original passwords.


Basic Auth

What is Basic Authentication?
    Basic Authentication is a simple and widely used method for providing authentication in HTTP-based applications. It is a way to authenticate and authorize users to access protected resources or perform certain actions.

What properties are necessary in the header of a Basic Auth request?
    In Basic Authentication, the client (usually a web browser) includes the user's credentials (username and password) in the "Authorization" header of the HTTP request. The credentials are encoded in Base64 format, which is a reversible encoding scheme but does not provide encryption or hashing for security.

How are username:password in Basic Auth encoded?
    In Basic Authentication, the username and password are encoded using Base64 encoding. The encoding process involves converting the username and password into a sequence of characters that can be safely transmitted over HTTP.

 OWASP auth cheatsheet

Define the authentication process to a non-technical recruiter.
     Authentication is the process of verifying the identity of a user or entity to ensure that they are who they claim to be. It is commonly used in various systems, such as websites, applications, and networks, to control access and protect sensitive information.
How should your error messaging respond (both HTTP and HTML)? Why?
    HTTP Response Status Codes: The HTTP response status code is a crucial part of error handling. It indicates the outcome of a request and helps the client understand the result. Commonly used HTTP status codes for error responses include:

    200 OK: Successful request
    400 Bad Request: Invalid or malformed request
    401 Unauthorized: Authentication is required or failed
    403 Forbidden: The client does not have permission to access the requested resource
    404 Not Found: The requested resource does not exist
    500 Internal Server Error: An unexpected error occurred on the server
 By returning the appropriate HTTP status code, the client can understand the nature of the error without parsing the response body. It enables automated systems and developers to handle errors programmatically
 
Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.