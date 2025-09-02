# Contributing

Thanks for considering contributing!

## Setup
1. Fork the repo and clone your fork.
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv .venv && source .venv/bin/activate
   pip install -r requirements.txt
   ```

## Branching & Commits
- Create feature branches from `main`: `feat/x`, `fix/y`.
- Use clear commit messages (e.g., Conventional Commits): `feat: add SMOTE step to pipeline`.

## Pull Requests
- Ensure the notebook runs end-to-end or provide a script in `src/`.
- Add/refresh screenshots in `docs/` if UI changes.
- CI must pass.

## Code Style
- Keep notebooks tidy (remove debug cells). Consider using `nbstripout`.
- For scripts, prefer type hints and docstrings.
