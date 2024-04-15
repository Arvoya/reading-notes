# Bearer-Authorization

## Questions & Answers

[Intro to JWT](https://jwt.io/introduction/)

1. What is a JSON Web Token (JWT)?
An open standard (RFC 7519) that defines a compact and self-contained way for securely
transmitting information between parties as a JSON object.
2. When shouold we use JSON Web Tokens?
Authorization and information exchange.
3. Claims are expected in which structural component of a JWT?
Sructural component of a JWT is the payload:
     - Header
     - Payload - **Claims**
     - Signature

---

[Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

1. If I get a JWT and I can decode the payload, how can we call that secure?
Because the payload is tied to a secret key that you would need to change the payload.
2. If sending a JWT, what must sender and reciever both know? Hint, it's appended
in the signature.
The secret key.
3. Explain how concatenated content and secret can be sent and recieved securely
to a non-technical recruiter.
The secret key is used to encode the content. Then everything is sent to the reciever.
The reciever uses the secret key to decode. If the content was changed, the signature
would not match anymore.

---

[JWT's Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

1. Why use JWT?
It is a way to securely transmit information between parties.
2. JWT is Compact and self-contained. Describe how this is useful to a non-technical
friend.
It is compact in the sense that you can send it in a URL, POST parameter, or an HTTP.
It's self-contained in the sense that it has all the information needed to verify the
information.
