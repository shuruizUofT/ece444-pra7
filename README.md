# ECE444 PRA7 — Static Analysis and CI with Ruff

Fork this repository to begin the practical. The starter includes a calculator,
two tests, and pinned development dependencies. You will configure Ruff,
pre-commit, and GitHub Actions during the lab.

## Environment

This lab was tested with **Python 3.15.2**. The commands below use Python 3.15.

## Start

### 1. Fork and clone locally

Fork this repository into your personal GitHub account.

In your terminal, clone your fork and enter its folder. Replace `YOUR_USERNAME`
with your GitHub username:

```sh
git clone https://github.com/YOUR_USERNAME/ece444-pra7.git
cd ece444-pra7
```

### 2. Set up the environment and run tests

Choose **one** command block for your platform. Each creates an isolated environment,
installs the pinned tools, and runs the starter tests.

**macOS / Linux**

```sh
python3.15 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements-dev.txt
python -m pytest -q
```

**Windows — PowerShell**

```powershell
py -3.15 -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements-dev.txt
python -m pytest -q
```

**Windows — Command Prompt**

```bat
py -3.15 -m venv .venv
.venv\Scripts\activate.bat
python -m pip install -r requirements-dev.txt
python -m pytest -q
```

On a new fork, expect **2 passed**. If you are verifying a completed fork, your
added tests should also pass. Keep the environment active for the activities.

### 3. Open the activity handout

In your computer’s file manager, open your cloned `ece444-pra7` folder, then the
`docs` folder. Open **index.html in a web browser**. If your editor opens the source
instead, use your file manager’s **Open With** option and choose a browser.
The [file on GitHub](docs/index.html) displays HTML source rather than the rendered handout.

Continue with **1) Configure static analysis and formatting**. Templates and the
flawed code sample are in `lab-assets/`; you will create the active configurations
and workflow during the activities.

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
