# Contributing to ReliefGrid

Thanks for helping improve this educational prototype.

## Workflow

1. Create a branch from `main` using a descriptive name such as `feat/inventory-filters` or `fix/api-validation`.
2. Keep pull requests focused and explain the user-visible change.
3. Add or update tests for behavior changes.
4. Run the checks listed in the README.
5. Never include real personal data, credentials, or emergency incident data.

## Code conventions

- Python: type hints for public helpers, validate untrusted inputs, and use parameterized SQL through `sqlite3`.
- JavaScript: keep DOM updates escaped, use accessible labels, and preserve offline demo behavior.
- CSS: keep shared styles in `assets/css/styles.css`; do not re-embed the stylesheet into HTML.
- SQL: update `backend/schema.sql` and tests when schema behavior changes.

## Scope and safety

ReliefGrid is not approved for emergency operations. Avoid describing fictional sample data as live or verified.
