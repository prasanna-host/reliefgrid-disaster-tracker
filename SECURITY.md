# Security Policy

## Scope

ReliefGrid is an educational prototype. It is not designed or approved for production or emergency response. The local Flask server does not provide user authentication, authorization, CSRF protection for deployment, rate limiting, or hardened operational logging.

## Reporting

Please do not publish credentials, private data, or real emergency information in issues. For a classroom project, report bugs privately to the repository maintainer or open a sanitized issue without sensitive information.

## Safe use

- Use fictional sample records only.
- Do not expose the development server directly to the public internet.
- Do not put secrets into source code or `.env` files under version control.
- Review and harden the system before any external deployment.
