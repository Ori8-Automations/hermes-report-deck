# Working in this repo

Report Deck, the Markdown report browser plugin for the Hermes Dashboard, live on the Ori8 Hermes
dashboard. `README.md` explains how to install it and documents its API and safety posture.

- Mission Control Dashboard (`Ori8-Automations/missioncontroldashboard`) carries a port of this
  plugin, so a change here may need porting there too.
- The reports in `sample-reports/` are made up, and the smoke test reads them. They must stay made
  up: never replace them with real agent output.
- Run the checks with `./tests/run_tests.sh`. It needs a Python with `fastapi` and `httpx`; point
  `PYTHON` at a venv that has them, e.g. `PYTHON=/path/to/venv/bin/python ./tests/run_tests.sh`.
- This repo is public. Never commit client names, internal hostnames or IP addresses, credentials,
  or real reports.
- Start from the default branch, `main`. When the work is done, open a pull request into `main` and
  tell Mike it is ready to merge. Finished work should never be left on a branch without a pull request.
