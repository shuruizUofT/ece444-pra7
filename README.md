# ECE444 PRA7 — Static Analysis and CI with Ruff

Fork this repository to begin the practical. The starter includes a calculator,
two tests, and pinned development dependencies. You will configure Ruff,
pre-commit, and GitHub Actions during the lab.

## Start

1. Fork this repository into your personal GitHub account.
2. Run the commands below, replacing `YOUR_USERNAME` with your GitHub username.
   They clone your fork, create a Python 3.15 environment, install the tools, and run the baseline tests:

```sh
git clone https://github.com/YOUR_USERNAME/ece444-pra7.git
cd ece444-pra7
python3.15 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements-dev.txt
python -m pytest -q
```

On Windows, create the environment with `py -3.15 -m venv .venv` and activate
with `.venv\Scripts\Activate.ps1` (PowerShell) or
`.venv\Scripts\activate.bat` (Command Prompt).

On a new fork, both starter tests should pass. If revisiting a completed fork, your added tests should also pass. Continue with **1) Configure static analysis and formatting**
in the lab handout: [docs/index.html](docs/index.html). Download or open that HTML
file in a browser to read it. Templates and a flawed code sample are in `lab-assets/`. The active Ruff configuration,
pre-commit configuration, and CI workflow are tasks you will complete during the activities.


## What the setup commands do

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


## Contents

- `calculator.py`: initial application code.
- `test_calculator.py`: two baseline tests.
- `requirements-dev.txt`: pinned Ruff, pre-commit, and pytest releases.
- `.gitignore`: excludes environments and generated caches.
- `lab-assets/`: configuration templates and the deliberately flawed code sample.
- `docs/index.html`: activity directions, checkpoints, and submission requirements.

## Attribution

This practical is adapted in structure from
[STAT 4160: Data Science Productivity Tools, Session 14 — pre-commit & GitHub Actions CI](https://ywanglab.github.io/STAT4160/lec14.html).
The calculator examples and ECE444 instructions were prepared for this practical.
