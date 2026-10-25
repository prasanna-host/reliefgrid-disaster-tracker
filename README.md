# ReliefGrid — Disaster Relief Resource Tracker

[![Project Quality Checks](https://github.com/prasanna-host/reliefgrid-disaster-tracker/actions/workflows/quality.yml/badge.svg)](https://github.com/prasanna-host/reliefgrid-disaster-tracker/actions/workflows/quality.yml)

ReliefGrid is a student-built, responsive front-end prototype for demonstrating how relief coordinators could review sample shelter capacity, track resource requests, and monitor supply inventory from one workspace.

> **Prototype disclaimer:** All people, places, counts, and requests are fictional sample data. This repository is not an emergency-response service. It has no backend, authentication, live location feed, dispatch integration, or operational guarantees. Do not use it to make real-world emergency decisions.

## Features

- Overview dashboard with request, shelter, occupancy, and low-stock summaries.
- Request register with search, priority/status filters, and resolve/reopen controls.
- Create a resource request with basic form validation.
- Export the request register to CSV.
- Shelter directory with capacity indicators.
- Inventory thresholds and visual low-stock warnings.
- Adjust inventory up or down, preventing stock from becoming negative.
- Export the inventory register to CSV.
- Local browser persistence for demo requests, inventory adjustments, shelters, and activity when browser storage is available.
- Responsive layout and light/dark color-scheme support.
- Automated static checks through GitHub Actions.

## Run locally

No package manager or build step is required.

1. Download or clone the repository.
2. Open `index.html` in a modern browser.
3. Navigate between Overview, Requests, Shelters, and Inventory.

For a more consistent browser storage origin, serve the repository from a local static server instead of opening the file directly. For example, with Python installed:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Data and privacy

The application is currently a client-side demo. It uses browser `localStorage` when available; that data is local to the browser profile and site origin, is not shared with other users, and can be cleared by clearing that site's browser data. There is no server database or account system. Do not enter personal, confidential, or real incident data.

## Repository layout

```text
.
├── index.html
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── ARCHITECTURE.md
│   ├── FEATURES.md
│   ├── PROJECT_OVERVIEW.md
│   ├── ROADMAP.md
│   └── TESTING.md
├── scripts/
│   └── validate_project.py
├── tests/
│   └── test_project.py
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md
    │   └── feature_request.md
    ├── pull_request_template.md
    └── workflows/
        └── quality.yml
```

## Quality checks

The project uses Python's standard library only for repository checks. Run:

```bash
python scripts/validate_project.py
python -m unittest discover -s tests -v
```

GitHub Actions runs these commands when changes are pushed or a pull request is opened against `main`.

## Roadmap

See [`docs/ROADMAP.md`](docs/ROADMAP.md) for planned work. Any real deployment would require a separately designed and reviewed backend, authentication and role-based permissions, audit logging, validation, secure operations, accessibility testing, and formal emergency-management partner review.

## Contributing

Read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening a pull request. Keep changes scoped, describe how they were tested, and update documentation when behaviour changes.

## License

See [`LICENSE`](LICENSE) for the repository's license.
