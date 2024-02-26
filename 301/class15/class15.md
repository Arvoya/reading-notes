# Authentication

[Module301](../README.md)

Reading assignment for class15.

## Questions and Answers

[What OAuth](https://www.csoonline.com/article/562635/what-is-oauth-how-the-open-authorization-framework-works.html)

1. What is OAuth? an open-standard authorization protocol/framework. It describes how unrelated servers and services can safely access to assets without sharing the credentials.
2. Give an example of what using OAuth would look like. Using Google Login to connect with various websites.
3. How does OAuth work? What are the steps that it takes to authenticate the user?
	1. First website connects to the second website on behalf of the user
	2. The second site generates a one-time Token and a one-time secret unique 
	3. First site gives this token and secret to the user's client software
	4. Client presents the request token and secret to their authorization provider
	5. May or may not require further authentication.
	6. User approves the transaction type
	7. User given approved access token
	8. User gives that access token to the first website
	9. Second website now lets the first website access the site on behalf of the sure
	10. User sees it all working together!
4. What is OpenID? It is an authentication standard that allows users to be authenticated. 

---

[Authorization and Authentication flows](https://auth0.com/docs/get-started/authentication-and-authorization-flow)

1. What is the difference between authorization and authentication? 
	* **Authentication** - verifies a user's identity to confirm they are who they claim to be.
	* **Authorization** - determines what resources and operations an authenticated user can access or perform.
1. What is Authorization Code Flow? A secure process where an authorization code is exchanged for a token, ensuring the token is obtained directly by the server without exposing the client secret.
2. What is Authorization Code Flow with Prof Key for Code Exchange (PKCE)? Enhances security for mobile and native application by using a high-entropy cryptographic string (code verifier) to handle attacks, giving Authorization Code more security. 
3. What is Implicit Flow with Form Post? A simplified OAuth 2.0 flow for public clients that cannot securely store client secrets, directly returning tokens post-authentication. It's less secure and not recommended for new applications. 
4. What is Client Credentials Flow? Allows applications to authenticate and authorize themselves for machine-to-machine (M2M) communication, obtaining an access token directly from the Authorization Server without a user login.
5. What is Device Authorization Flow? Designed for devices with no browser or limited input capabilities, it allows indirect user authorization via a separate device with a browser, simplifying login for devices like smart TVs or IoT devices.
6. What is Resource Owner Password Flow? A flow where users directly provide their credentials (username and password) to highly-trusted applications, allowing these applications to obtain an access token. This flow bypasses the need for redirecting users for authentication but is less secure and recommended only when other flows are not viable.

