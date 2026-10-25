# ReliefGrid — Disaster Relief Resource Tracker

ReliefGrid is a student-built front-end prototype for coordinating disaster-relief resources. It presents a shared dashboard for sample shelter occupancy, supply inventory, and field-team requests.

> **Important:** This repository currently contains a browser-only demonstration. It uses fictional sample data and does not connect to emergency services, live maps, real shelters, dispatch systems, or a backend. Do not use it to coordinate a real emergency.

## Features

- Dashboard overview with summary metrics.
- Shelter directory with illustrative occupancy and capacity.
- Resource-request form with priority selection.
- Request filtering by priority.
- Inventory snapshot and replenishment thresholds.
- Recent activity list for the current page session.
- Responsive layout for desktop and mobile.
- HTML escaping for user-entered values before rendering.

## Run locally

No package installation or build process is required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Use **Create resource request** to add a sample request.
4. Navigate between Overview, Requests, Shelters, and Inventory.

For a local web server (optional), run:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Project structure

```text
reliefgrid-disaster-tracker/
├── index.html
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── SECURITY.md
├── .gitignore
├── docs/
│   ├── PROJECT_OVERVIEW.md
│   ├── FEATURES.md
│   ├── ARCHITECTURE.md
│   ├── ROADMAP.md
│   └── TESTING.md
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        └── feature_request.md
```

## Technology

- HTML5
- CSS3 (responsive layout and custom properties)
- Vanilla JavaScript (no runtime dependencies)

## Known limitations

- Data is stored in in-memory JavaScript arrays and resets when the page is reloaded.
- There is no authentication, role-based access, API, database, or multi-user synchronization.
- The map is an illustrative SVG, not a geographic or routing service.
- Sample counts and locations are fictional.

## Future development

See [`docs/ROADMAP.md`](docs/ROADMAP.md). Suggested next steps include persistent storage, a backend API, authentication and authorization, verified location data, audit history, accessibility checks, and automated tests.

## Contributing

Read [`CONTRIBUTING.md`](CONTRIBUTING.md). Use a feature branch and submit a pull request for changes.

## License

This project is released under the MIT License. See [`LICENSE`](LICENSE).
