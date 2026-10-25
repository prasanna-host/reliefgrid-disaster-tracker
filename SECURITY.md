# Security Policy

## Scope

ReliefGrid is an educational, client-side prototype with fictional data. It has no backend, account system, live feeds, or production emergency-response capability.

## Reporting a concern

Please do not include real personal information, credentials, or sensitive incident details in a public issue. For a non-sensitive code concern, open a GitHub issue with a minimal reproduction. For a sensitive concern, contact the repository owner privately through GitHub before publishing details.

## Current limitations

- Browser-local storage is not a secure data store.
- There is no authentication, authorisation, server-side validation, or audit-grade history.
- No production availability, integrity, or confidentiality guarantees are offered.
- The application must not be used to direct real emergency operations.

## Safe-development practices

- Keep sample data fictional.
- Escape user-controlled text before HTML rendering.
- Validate values before mutating local state.
- Do not commit secrets or private data.
- A real deployment would require threat modelling, security review, server-side access controls, audit trails, backups, monitoring, and an incident-response process.
