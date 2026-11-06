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

## How to work through this lab

You may copy and paste the setup commands. Environment setup is preparation;
the learning objectives are understanding static analysis and continuous integration.
Read each command before running it:

| Command | Purpose |
| --- | --- |
| `git clone <your-fork-url>` | Download your own fork to your computer. |
| `cd ece444-pra7` | Enter the project directory. |
| `python3.15 -m venv .venv` | Create an isolated Python environment for the lab. |
| `source .venv/bin/activate` | Activate that environment on macOS/Linux. |
| `python -m pip install -r requirements-dev.txt` | Install the pinned development tools. |
| `python -m pytest -q` | Verify that the two baseline tests pass. |

For the assessed work, use the provided examples as starting points and make
sure you can explain your choices:

1. **Configure Ruff:** explain what each enabled rule family checks and why it
   belongs in the configuration.
2. **Investigate findings:** run Ruff, interpret the reported rule codes, and
   repair the code. Distinguish automatic fixes from changes requiring your judgment.
3. **Configure CI:** identify the commands that perform linting, formatting checks,
   and tests in the workflow. Explain what causes each check to fail.
4. **Verify the result:** provide evidence of a failed check, your repair, and a
   passing pull request. Explain why tests can pass while static analysis fails.

Copying a configuration or workflow alone does not demonstrate understanding.
Your explanations and the failed-to-passing evidence are part of the lab work.

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
