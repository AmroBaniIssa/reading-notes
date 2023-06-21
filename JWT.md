What is a JSON Web Token (JWT)?
  A JSON Web Token (JWT) is a compact and self-contained means of transmitting information between parties as a JSON object. It is commonly used for authentication and authorization purposes in web applications.
  
  JWTs consist of three parts: a header, a payload, and a signature. The header specifies the hashing algorithm used to secure the token, the payload contains the claims or information about the user or entity, and the signature is used to verify the integrity of the token.

When should we use JSON Web Tokens?
  Authentication: JWTs are commonly used for user authentication. When a user logs in, the server can issue a JWT containing user information (claims) and send it back to the client. The client can then include the JWT in subsequent requests to authenticate and access protected resources.

  Authorization and Access Control: JWTs can carry authorization information such as user roles, permissions, or access rights. The server can validate the JWT and its claims to determine whether the user has the necessary privileges to access specific resources.

Claims are expected in which structural component of a JWT?
  Claims are expected to be present in the payload component of a JSON Web Token (JWT). The payload is a JSON object that contains the claims or statements about the entity (typically the user) and additional metadata. It consists of key-value pairs, where the keys represent the claim names and the values represent the claim values.
  It's important to note that the claims in the payload are not encrypted or protected by default. They are encoded using Base64Url encoding, which can be easily decoded. Therefore, sensitive information should not be included in the claims unless the JWT is encrypted or transmitted over a secure channel.

If I get a JWT and I can decode the payload, how can we call that secure?
   Here are a few points to consider regarding the security of JWTs:
   -Integrity: JWTs are typically signed using a digital signature (using a secret key or a public/private key pair), which ensures the      integrity of the token. When a JWT is received, it can be verified using the signature to ensure that it has not been tampered with. If the signature is invalid, the token is considered compromised and should be rejected.
   -Confidentiality: While the payload of a JWT is easily readable when decoded, the content of the payload can still be considered confidential if it contains sensitive information. To protect the confidentiality of the payload, JWTs can be encrypted using encryption algorithms. Encrypted JWTs ensure that the payload remains confidential even if intercepted by unauthorized parties.
   -Secure Transmission: JWTs should be transmitted over secure channels, such as HTTPS, to prevent interception or eavesdropping by attackers. By using secure communication protocols, you can ensure that the token remains secure during transit.
   -Limited Lifetime: JWTs have an expiration time (defined by the "exp" claim) that limits their validity period. Once a JWT expires, it should no longer be considered valid. This helps mitigate the risk of unauthorized access to protected resources if a JWT is somehow obtained by an attacker.

If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
   When sending a JWT, the sender and receiver must both know the secret key used for signing the token. The secret key is a shared secret between the sender (issuer) and the receiver (verifier) of the JWT.

Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
   Imagine you have a message that you want to send to someone securely, and you also want to include a secret piece of information. To ensure that only the intended recipient can access the message and the secret, we use a process called encryption.

   Encryption is like putting the message inside a locked box that only the recipient can open. The box requires a special key to unlock it. In our case, the message represents the concatenated content and the secret, and the key is a unique piece of information known only to the sender and the recipient.

   Before sending the message, the sender uses encryption software to transform the concatenated content and the secret into an unreadable format, often referred to as ciphertext. This ciphertext can only be deciphered and understood with the corresponding key, which remains a secret.

   Once the ciphertext is sent to the recipient, they receive it and use a decryption process to convert the unreadable ciphertext back into the original concatenated content and secret. This decryption process requires the special key that matches the one used for encryption.

   By using encryption and keeping the key confidential, we ensure that even if someone intercepts the message, they won't be able to understand the content or access the secret without the proper decryption key.

JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
   Compactness: A JWT is like a small package that contains all the important information needed for authentication. It's compact because it doesn't contain unnecessary or redundant data. JWT contains all the necessary information in a concise format.
   Self-contained: The information inside the JWT is self-contained, meaning it carries everything needed for authentication and authorization. It's like a magic token that holds all the required details securely.The JWT itself holds your identity and any necessary access permissions.

What are the three components (the structure) of a JWT signature?
   Header: The header of a JWT contains information about the type of token and the signing algorithm used. It is encoded using Base64Url and typically includes the following two properties:
     "alg" (algorithm): Specifies the algorithm used for signing the token, such as HMAC, RSA, or ECDSA.
     "typ" (type): Specifies the type of token, which is "JWT" for JSON Web Tokens.

   Payload: The payload, also known as the claims or the body, contains the actual information or data that is being transmitted within the token. It can include various properties or claims about the user or the token itself. Some common standard claims include:
    "iss" (issuer): Specifies the entity that issued the token.
    "sub" (subject): Identifies the subject of the token, typically the user.
    "exp" (expiration time): Specifies the expiration time of the token.
    "iat" (issued at): Indicates the time at which the token was issued.
     The payload is also encoded using Base64Url encoding to ensure it can be transmitted safely.

   Signature: The signature is created by taking the encoded header, the encoded payload, and a secret or a private key and applying a specific signing algorithm. The purpose of the signature is to ensure the integrity and authenticity of the token. Only the party possessing the secret or private key can generate a valid signature, allowing the receiver to verify the token's authenticity.