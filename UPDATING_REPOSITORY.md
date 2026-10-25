# Update the GitHub repository from the browser

This pack contains an updated `index.html`, refreshed documentation, and new quality-check files. It is designed to be uploaded to the existing repository without Git commands.

## 1. Download and extract

Download `reliefgrid-professional-update-pack.zip` and extract it on your computer. Keep the directory structure intact, including `.github`, `docs`, `scripts`, and `tests`.

## 2. Upload to your existing repository

1. Open https://github.com/prasanna-host/reliefgrid-disaster-tracker/.
2. Select the `main` branch (or preferably create a branch named `feat/professional-demo-updates` first if you're making a PR).
3. Choose **Add file → Upload files**.
4. Drag the extracted files and folders into the upload area. Preserve their relative paths. Make sure hidden/dot-prefixed paths such as `.github/` and `.gitignore` are included.
5. Replace existing files with the same paths when prompted. The main updated app is `index.html`.
6. Add a commit message such as `feat: improve request and inventory workflows`.
7. If using a branch, commit to that branch and open a pull request into `main`. If uploading directly to `main`, the change will not create a PR.

## 3. Confirm the workflow is running

After the commit or PR is created, open the repository's **Actions** tab. The `Project Quality Checks` workflow should run the static validator and six regression tests. A green check means those automated checks passed; it does not replace manual browser testing.

## Important notes

- Existing `LICENSE` is deliberately not included in this update pack, so your repository's current license remains untouched.
- This pack includes updated `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `.gitignore`, and files under `docs/`; review those changes before committing.
- The app is still a front-end prototype using fictional sample data. Browser storage is local to one browser profile/origin, not a shared backend.
- Do not upload real emergency data, private information, API keys, or credentials.
