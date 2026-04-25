🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# ☕ Soc Ops

> Pull up a chair. Break the ice. Get 5 in a row.

A warm, conversational social bingo game built with **FastAPI**, **Jinja2**, and **HTMX**—perfect for workshops, mixers, and learning how to build server-driven interactivity that just *feels right*.

---

## 🏡 What's this all about?

Imagine walking into a room where everyone's chatting, warm drinks in hand, and someone mentions a game. Soc Ops brings that vibe to your browser. Click squares with prompts like "Find someone who's tried fermentation" or "Chat with someone who's traveled to 3+ countries." Get five in a row. Celebrate together.

Under the hood, it's a masterclass in building modern web experiences: session state on the backend, HTMX for instant updates, and templates that talk to each other like they're old friends.

---

## 🎯 Why build this?

- **Learn real patterns:** FastAPI + Jinja2 + HTMX is a timeless combo for serverside rendering that doesn't feel clunky.
- **Play with state:** Session management, game logic, and reset flows all handled cleanly in `app/game_service.py`.
- **Perfect for demos:** Great for showing off AI-aided design, refactoring, or just how fast you can iterate.

---

## 📦 Room tour

```
app/
  main.py           # FastAPI routing and session setup
  game_service.py   # Where the game logic lives (session state, scoring)
  models.py         # Game state enums
  templates/        # Jinja2 fragments (startup, board, modals)
  static/
    css/app.css     # Utility-style CSS, easy to extend
    js/htmx.min.js  # Instant updates without page reloads
```

---

## 🚀 Get cozy, get started

**Prerequisites:** Python 3.13+, `uv`

```bash
cd /workspaces/agent-lab-python
uv sync
uv run pytest
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Then crack open your browser at `http://localhost:8000` and say hello to the game board.

---

## 🧭 Journey through the workshop

Each part builds on the last, with hands-on tasks and design decisions to think through:

| Part | What you'll do |
|------|---|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Get the lay of the land & tick the boxes |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Wire up the backend, write good instructions |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Craft the UI, polish the experience |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Add a custom question engine |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Orchestrate multiple agents |

> Want to read offline? The full workshop lives in the `workshop/` folder.

---

## 🤝 Built with love (and these tools)

- **FastAPI** — modern, fast web framework
- **Jinja2** — templating that doesn't get in the way
- **HTMX** — real-time UI updates without JavaScript boilerplate
- **Python 3.13+** — clean, readable backend code
- **Uvicorn** — production-grade server

---

## 🎨 Want to experiment?

The codebase is structured for change. Tweak the CSS, add new prompts, refactor the game logic—everything's designed to be readable and extensible. Start with the test suite: `uv run pytest`. Then explore.

---

[🔗 Full workshop on Copilot Dev Days](https://copilot-dev-days.github.io/agent-lab-python)
