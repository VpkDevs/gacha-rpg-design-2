# Repo guide for AI coding agents (Auto-generated)

## Purpose ✨
- Help AI agents be immediately productive in this repository by describing the project's focus, structure, and actionable developer workflows.

## Quick facts (what to know first) ✅
- This repository is primarily a **game design / planning repo** (mobile gacha-roguelite). Key design docs live at the repo root, e.g. `game_design_document.md`, `complete_game_design.md`, and `Advanced-Monetization-&-Psychology-Strat.md`.
- Minimal code exists: the `src/` package contains only `__init__.py` and tests live in `tests/test_sample.py` (uses Python's `unittest`).
- A lightweight CI workflow runs unit tests with GitHub Actions on push and pull_request (see `.github/workflows/python-tests.yml`).
- PR and issue templates are available (`.github/PULL_REQUEST_TEMPLATE.md`, `.github/ISSUE_TEMPLATE/bug_report.md`).
- The repo includes an `AGENT-INITIALIZE.prompt` that outlines how an agent should perform multi-phase project analysis — treat this as canonical for large-scope tasks.

## How to get started (concrete commands) 🔧
- Run tests: `python -m unittest discover -s tests` (the project uses `unittest` in `tests/`).
- CI: `python -m unittest discover -s tests` is executed by GitHub Actions on push and pull requests (`.github/workflows/python-tests.yml`).
- Install dependencies: inspect `requirements.txt` (currently empty). When adding packages, update `requirements.txt` and include pinned versions.
- For local development, add new modules under `src/` and ensure `src/__init__.py` exports or documents them.

## Project-specific conventions & patterns 🧭
- Documentation-first project: most work will be editing or adding markdown design documents. Keep updates concise and preserve section structure (e.g., Core Concept, Gameplay Loops, Monetization).
- Tests: any code change should include at least one `unittest` in `tests/`. Use simple unit tests (see `tests/test_sample.py` for format).
- Minimal packaging: there is no package or build configuration (no `setup.py`, `pyproject.toml`, or CI). If you add packaging, update README and `requirements.txt`.

## Where to make changes (key files to reference) 📁
- Design & specs: `game_design_document.md`, `complete_game_design*.md`, `Advanced-Monetization-&-Psychology-Strat.md`
- Agent guidance: `AGENT-INITIALIZE.prompt` — follow its phased approach (analysis → planning → execution) for cross-cutting tasks
- Code: `src/` (new python modules should be added here)
- Tests: `tests/` (use `unittest` tests)
- Repo metadata: `README.md`, `requirements.txt` (keep them up to date with code changes)

## Recommended agent workflow (short & actionable) 🛠️
1. Read `AGENT-INITIALIZE.prompt` to align on discovery & planning phases.
2. Scan root `*.md` files to understand the game design goals before proposing code or doc changes.
3. If adding code, create a small module in `src/`, add `unittest` in `tests/`, run `python -m unittest discover -s tests` and verify tests pass.
4. Update `README.md` with installation/run instructions and record any added dependencies in `requirements.txt`.
5. When proposing larger changes (new features, CI, packaging), include a short design note in a new `docs/` or `design/` markdown file and a concise PR description referencing the change impact.

## Examples of useful edits (examples from this repo) 💡
- Add a gameplay simulation module: `src/simulate_run.py` + `tests/test_simulate_run.py` (use `unittest` and include deterministic seeds in tests).
- Expand `requirements.txt` when introducing libraries (e.g., `pytest==X.Y.Z` or `numpy==X.Y.Z`) and reflect usage in `README.md`.
- Add small design notes or proposals as new files under `docs/` or `design/` (e.g., `docs/gacha-rate-proposal.md`) and reference related design docs.

---

## Quick checklist for PRs ✅
- Include a short motivation and the high-level change in the PR description.
- If code changes: add/adjust tests in `tests/` and update `requirements.txt` if new deps are added.
- If design changes: update the affected `*.md` design file and add a short changelog entry.

## Questions or feedback? 💬
If anything in this guide is unclear or you find gaps, please open a short issue or add comments in a PR — I’ll iterate on this guidance.
 