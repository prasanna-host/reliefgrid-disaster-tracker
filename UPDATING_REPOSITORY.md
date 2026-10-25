# Update the GitHub repository (browser-only)

This ZIP is a **complete replacement layout**, not just a small patch. It separates the old single-file prototype into a real frontend plus a Python/SQLite backend.

## Recommended upload flow

1. Download and extract this ZIP on your computer.
2. Open the GitHub repository and create a branch such as `feat/python-sqlite-stack`.
3. Use **Add file → Upload files** and upload the contents of this extracted project while preserving folders. Do not upload only `index.html`, and do not upload the ZIP itself.
4. Replace the existing `index.html`, `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `LICENSE`, `.gitignore`, and `CHANGELOG.md` with the versions in this pack. Add all new folders and files.
5. Commit the upload to the feature branch, create a pull request into `main`, and review the file list before merging.
6. After merging, open the **Actions** tab and check that **Project Quality Checks** passes.
7. Once the new `index.html` works, delete the old `ReliefGrid — Disaster Relief Tracker.html` root file. It is the bundled single-file prototype; leaving it in the repository can keep the language statistics heavily skewed toward HTML.

## Important deployment change

The professional version uses a Python/Flask backend to serve the UI and SQLite API. A GitHub Pages site cannot run Flask or SQLite by itself. For the full version, run it on a Python-capable host or locally following the README. Static hosting will show the UI, but API persistence will be unavailable and the browser-local fallback will be used.

Do not delete your repository or use GitHub's web editor to paste all the files into a single HTML file. The folders are now part of the architecture.
