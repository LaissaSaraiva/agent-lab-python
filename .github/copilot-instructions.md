# Workspace Instructions for AI Coding Agents

## Mandatory development checklist
- `uv sync`
- `uv run ruff check .`
- `uv run pytest`

## Project overview

FastAPI + Jinja2 + HTMX social bingo game. Session-based state lives in `app/game_service.py`; templates are in `app/templates/`; CSS utilities are in `app/static/css/app.css`.

## Key conventions
- Use `uv` for dependency and task running.
- Verify frontend in an external browser; do not use VS Code Simple Browser.
- HTMX fragments rely on server-rendered POST responses.
- Preserve session flow and template fragment behavior when changing routes.

## Common commands
- `uv sync`
- `uv run pytest`
- `uv run ruff check .`
- `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`

## Notes
- `app/main.py` hosts routing and session middleware.
- `app/models.py` defines game state enums.
- `app/templates/components/` renders the interactive board and modals.
- `pyproject.toml` defines the `soc-ops` script entrypoint.
