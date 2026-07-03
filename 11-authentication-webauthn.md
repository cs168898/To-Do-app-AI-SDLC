# WebAuthn/Passkeys Authentication

## Scope

- Passwordless authentication with WebAuthn passkeys.
- Registration and login using platform biometrics/security keys.
- JWT-based session management.
- Route protection middleware.

## Functional Requirements

1. **Registration**
   - Generate challenge and register a new credential via WebAuthn ceremony.
   - Persist credential public key and metadata.
2. **Login**
   - Generate challenge and verify assertion response.
   - Issue JWT on successful authentication.
3. **Session Management**
   - Use signed JWTs with expiration and secure transport/storage practices.
4. **Authorization**
   - Protect authenticated routes using middleware that validates JWTs.

## Security Requirements

- Challenges must be random, single-use, and short-lived.
- Verify RP ID/origin, challenge, signature, and counter semantics.
- Reject replayed assertions and malformed WebAuthn responses.
- Never log or expose sensitive auth artifacts.
