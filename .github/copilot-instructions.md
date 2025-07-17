# Copilot Instructions for skills-integrate-mcp-with-copilot

## Project Overview
This is a FastAPI-based web application for managing and signing up for extracurricular activities (see `src/app.py`). The project is designed for learning how to integrate Model Context Protocol (MCP) with GitHub Copilot.

## Architecture & Key Files
- **Backend:** Python FastAPI app (`src/app.py`)
- **Frontend:** Static files served from `src/static/` (`index.html`, `app.js`, `styles.css`)
- **API Docs:** Auto-generated at `/docs` and `/redoc` when running locally
- **Workflows:** GitHub Actions in `.github/workflows/` automate exercise steps and feedback

## Developer Workflows
- **Install dependencies:**
  ```sh
  pip install -r requirements.txt
  ```
- **Run locally:**
  ```sh
  uvicorn src.app:app --reload
  ```
- **Access API docs:**
  - [http://localhost:8000/docs](http://localhost:8000/docs)
  - [http://localhost:8000/redoc](http://localhost:8000/redoc)
- **Static site:**
  - Served from `/static` when app is running

## Patterns & Conventions
- **Activity Data Model:** Activities are identified by name; signups use email as a query parameter.
- **Endpoints:**
  - `GET /activities` — List all activities
  - `POST /activities/{activity_name}/signup?email=...` — Sign up for an activity
- **No database:** Data is likely stored in-memory for simplicity (see `app.py`).
- **Self-paced exercise:** Workflow files automate step progression and feedback via GitHub Issues/comments.

## Integration Points
- **MCP & Copilot:** The exercise is designed to teach expanding Copilot with MCP, but the main code is a simple FastAPI app.
- **GitHub Actions:** `.github/workflows/0-start-exercise.yml` and related files automate onboarding and feedback.

## Examples
- To add a new activity, update the activities data structure in `src/app.py`.
- To change signup logic, modify the relevant POST endpoint in `src/app.py`.
- To update the frontend, edit files in `src/static/`.

## References
- Main backend: [`src/app.py`](src/app.py)
- Frontend: [`src/static/index.html`](src/static/index.html), [`src/static/app.js`](src/static/app.js)
- Exercise workflow: [`.github/workflows/0-start-exercise.yml`](.github/workflows/0-start-exercise.yml)
- Project README: [`README.md`](README.md), [`src/README.md`](src/README.md)

---
If any section is unclear or missing, please provide feedback so instructions can be improved for future AI agents.
