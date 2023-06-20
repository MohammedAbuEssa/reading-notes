# Bearer Authorization

## [Intro to JWT](https://jwt.io/introduction/)

1. What is a JSON Web Token (JWT)?
   JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

2. When should we use JSON Web Tokens?

   a) Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

   b) Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

3. Claims are expected in which structural component of a JWT?
   Payload

---

## [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

1. If I get a JWT and I can decode the payload, how can we call that secure?
   JWTs can be either signed, encrypted or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore.

2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
   Shared Secret or Public Key.

3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
   Let's assume Alice wants to send a JWT to Bob. They both know some shared secret. Mallory doesn't know that secret, but wants to interfere and change the JWT. To prevent that, Alice calculates Hash(payload + secret) and appends this as signature.

---

[JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

1. Why use JWT?
   Securely transfer information between any tow bodies.

2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
   JWTs are like small, self-contained packages for sending information securely. You can put all the necessary data in a single string and send it to your friend without needing to share extra secrets or codes. They can easily access and verify the information without relying on external services. It's a convenient and user-friendly way to communicate securely.

3. What are the three components (the structure) of a JWT signature?
   a) Header.
   b) Payload.
   c) Signature.

[Main Page](../README.md)
