nestjs-auth0



#### **8.6 Authentication in NestJS with Auth0 \& JWT**



**How does Auth0 handle authentication compared to traditional username/password auth?**



&#x09;In traditional authentication, the backend is responsible for everything about users and passwords while in Auth0 this responsibility is delegated to a trusted identity provider, and your app only verifies tokens.



**What is the role of JWT in API authentication?**



&#x09;JWT's role in API authentication is to confirm user identity, carry user claims securely, enable stateless authentication, protect API routes via token validation, and improve scalability by removing session storage.



**How do jwks-rsa and public/private key verification work in Auth0?**



&#x09;JWT verification with Auth0 works by using JWKS to verify tokens signed with Auth0's private key, with jwks-rsa handling key retrieval and caching.



**How would you protect an API route so that only authenticated users can access it?**



&#x09;To protect an API route I would require a JWT in request headers, verify the token's signature and claims, attach user info to request, allow or deny access, and optionally enforce roles/permissions.

