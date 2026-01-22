# Project Title

A brief description of your project.

## Installation

Clone the repo and (optionally) create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # macOS / Linux
.\.venv\Scripts\Activate   # Windows (PowerShell)
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Usage

Run unit tests with:

```bash
python -m unittest discover -s tests
```

## Contributing

- Follow the `AGENT-INITIALIZE.prompt` process for analysis and planning when proposing larger work.
- Use the PR template (`.github/PULL_REQUEST_TEMPLATE.md`) and ensure tests pass locally before opening a PR.
- Keep design docs concise and update the relevant `*.md` files when making changes that affect game design.

## CI

A GitHub Actions workflow runs unit tests on push and PRs (`.github/workflows/python-tests.yml`).
