# ReliefGrid — Disaster Relief Resource Tracker

![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?logo=python&logoColor=white) ![Flask](https://img.shields.io/badge/Flask-REST%20API-black?logo=flask) ![JavaScript](https://img.shields.io/badge/JavaScript-ES2020-F7DF1E?logo=javascript&logoColor=222) ![SQLite](https://img.shields.io/badge/SQLite-persistent%20storage-003B57?logo=sqlite&logoColor=white) ![License](https://img.shields.io/badge/License-MIT-green)

ReliefGrid is an educational disaster-relief coordination prototype. It brings example shelter occupancy, incoming resource requests, inventory levels, and a recent-activity register into one dashboard. The codebase separates the frontend (HTML, CSS, JavaScript) from a Python/Flask API and SQLite data layer.

> **Safety notice:** All people, locations, counts, and needs are fictional sample data. This is not an emergency-response service and has no live dispatch, emergency feed, authentication, or operational guarantees. Do not use it for real-world emergency decisions.

## Features

- Responsive dashboard with sample shelter capacity and low-stock summaries.
- Request search and priority/status filters.
- Mark requests resolved and reopen them.
- Inventory adjustments with negative-stock protection and reorder-threshold warnings.
- CSV export for requests and inventory.
- Browser-local fallback when the Python API is unavailable.
- Flask REST endpoints backed by a relational SQLite database when run as a server.
- Input validation, transaction-based state updates, API tests, and GitHub Actions checks.

## Technology stack

| Layer | Technology | Responsibility |
|---|---|---|
| UI | HTML5 | Accessible page structure |
| Styling | CSS3 | Responsive layout and theme |
| Client behavior | JavaScript | Filtering, forms, exports, API synchronization |
| API | Python 3.11+ and Flask | Validation and HTTP endpoints |
| Persistence | SQLite and SQL | Requests, shelters, stock, activity |
| Automation | GitHub Actions YAML | Test and quality checks on pushes and pull requests |

## Run locally (Windows)

1. Install Python 3.11 or newer.
2. Open Command Prompt in this project folder.
3. Run:

   ```bat
   py -m venv .venv
   .venv\Scripts\activate
   python -m pip install -r requirements.txt
   python backend\app.py
   ```

4. Open http://127.0.0.1:5000 in your browser. The first start creates `instance/reliefgrid.sqlite3` and seeds fictional demo data.

## Run locally (macOS/Linux)

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python backend/app.py
```

Then open http://127.0.0.1:5000. Flask serves the UI and API from the same origin.

## API overview

| Method | Endpoint | Purpose |
|---|---|---|
| `GET` | `/api/health` | Health/status check |
| `GET` | `/api/state` | Read complete demo state |
| `PUT` | `/api/state` | Validate and save a state snapshot |
| `GET` | `/api/requests` | List requests |
| `POST` | `/api/requests` | Create a request |
| `PATCH` | `/api/requests/<id>` | Update a request status |
| `GET` | `/api/shelters` | List shelters |
| `GET` | `/api/inventory` | List inventory |
| `PATCH` | `/api/inventory/<item_name>` | Adjust stock by an integer `delta` |
| `GET` | `/api/activity` | List recent activity |

Example health check:

```bash
curl http://127.0.0.1:5000/api/health
```

Example inventory adjustment:

```bash
curl -X PATCH http://127.0.0.1:5000/api/inventory/Blankets \
  -H 'Content-Type: application/json' \
  -d '{"delta": 20}'
```

## Tests and checks

```bash
python -m unittest discover -s tests -v
python scripts/validate_project.py
node --check assets/js/app.js
```

GitHub Actions runs these checks automatically for pushes and pull requests.

## Repository structure

```text
.
├── index.html
├── assets/
│   ├── css/styles.css
│   └── js/app.js
├── backend/
│   ├── app.py
│   └── schema.sql
├── tests/test_api.py
├── scripts/validate_project.py
├── docs/
├── .github/workflows/quality.yml
├── requirements.txt
└── README.md
```

## Project status

This is a student/demo prototype. It currently has no login, authorization, deployment hardening, audit-grade record integrity, realtime synchronization, map/geocoding integration, or service-level guarantees. The included API is suitable for local learning and testing, not public emergency operations.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Please include tests for behavior changes and keep demo-only claims explicit.
