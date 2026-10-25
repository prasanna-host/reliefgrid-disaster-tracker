# Contributing to ReliefGrid

Thanks for helping improve this student project. Small, reviewable contributions are preferred.

## Before you start

- Read the project README and the relevant documents in `docs/`.
- Check open issues and pull requests so work is not duplicated.
- Open an issue first for large feature changes or architecture proposals.

## Development workflow

1. Create a branch from `main` with a descriptive name, such as `feat/inventory-export` or `docs/testing-guide`.
2. Keep a pull request focused on one change.
3. Update documentation and `CHANGELOG.md` when user-visible behaviour changes.
4. Run the checks below before opening a pull request.
5. Describe the motivation, implementation, test steps, and limitations in the PR.

## Local checks

```bash
python scripts/validate_project.py
python -m unittest discover -s tests -v
```

Open `index.html` in a modern browser and manually exercise the affected flow. If you change the UI, check a narrow/mobile viewport and the browser console.

## Contribution expectations

- Use semantic HTML and label controls for accessibility.
- Escape user-provided text before inserting it into HTML.
- Do not add real personal, location, or emergency incident data to examples.
- Do not represent sample information as live or verified.
- Avoid adding dependencies unless there is a clear need and the dependency is documented.
- Never commit secrets, API keys, credentials, or private data.

## Pull request checklist

- [ ] The change has one clear purpose.
- [ ] Existing functionality remains intact.
- [ ] Automated checks pass.
- [ ] Manual testing steps and results are included.
- [ ] Documentation/changelog updated where applicable.
- [ ] Limitations and any follow-up work are explained.
