# ECE444 PRA7 — Static Analysis and CI with Ruff

Fork this repository to begin the practical. The starter includes a calculator,
two tests, and pinned development dependencies. You will configure Ruff,
pre-commit, and GitHub Actions during the lab.

## Start

1. Fork this repository into your personal GitHub account.
2. Clone **your fork**, then enter its directory.
3. Create a Python 3.15 environment and install the dependencies:

```sh
python3.15 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements-dev.txt
python -m pytest -q
```

On Windows, create the environment with `py -3.15 -m venv .venv` and activate
with `.venv\Scripts\Activate.ps1` (PowerShell) or
`.venv\Scripts\activate.bat` (Command Prompt).

Both tests should pass. Continue with **1) Configure static analysis and formatting**
in the lab handout: [docs/index.html](docs/index.html). Download or open that HTML
file in a browser to read it. The repository intentionally has no Ruff configuration,
pre-commit configuration, or CI workflow yet.

When opening a pull request for the lab, set the base repository to
**your own fork**, not the instructor repository.

## Contents

- `calculator.py`: initial application code.
- `test_calculator.py`: two baseline tests.
- `requirements-dev.txt`: pinned Ruff, pre-commit, and pytest releases.
- `.gitignore`: excludes environments and generated caches.
- `docs/index.html`: complete lab handout.

## Attribution

This practical is adapted in structure from
[STAT 4160: Data Science Productivity Tools, Session 14 — pre-commit & GitHub Actions CI](https://ywanglab.github.io/STAT4160/lec14.html).
The calculator examples and ECE444 instructions were prepared for this practical.
