# ECE444 PRA7 — Static Analysis and CI with Ruff

Fork this repository to begin the practical. The starter includes a calculator,
two tests, and pinned development dependencies. You will configure Ruff,
pre-commit, and GitHub Actions during the lab.

## Before setup

Install [Python 3.15.2](https://www.python.org/downloads/release/python-3152/)
and a recent [Git](https://git-scm.com/downloads) (2.31 or newer). Reopen your
terminal after installation. Check that the commands are available:

```sh
python3.15 --version
git --version
```

On Windows, use `py -3.15 --version` instead. If a command is not found, complete
the installation and ensure it is on your PATH before continuing. On macOS,
if Git reports an Xcode license or developer-tools error, follow your system’s
setup instructions or install Git from the link above.

You also need a GitHub account. Before your first commit, check your Git identity:

```sh
git config user.name
git config user.email
```

If either is empty, after cloning your fork run the following **inside that clone**,
replacing the example values with your own name and GitHub-associated email
(or your GitHub-provided private noreply address):

```sh
git config user.name "Your Name"
git config user.email "YOUR_EMAIL"
```

These settings identify your commits; they do not sign you into GitHub. When
pushing for the first time, follow GitHub’s sign-in prompt. An account password
is not accepted for Git HTTPS authentication; see
[GitHub authentication guidance](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github).

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

## Troubleshooting

- **`No module named ruff` or `pytest`:** reactivate `.venv` and install `requirements-dev.txt` again.
- **`unknown option deduplicate`:** your Git is too old for pre-commit. Install a recent Git, restart the terminal, and check `git --version`.
- **A hook changed files:** review the changes, run `git add` on the changed files, and retry the check or commit.
- **PowerShell blocks environment activation:** use Command Prompt and `.venv\Scripts\activate.bat` instead.
- **An expected failing command returns a nonzero exit code:** read its report and proceed to the next lab step; run demonstration commands one at a time.
