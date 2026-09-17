# Medical Appointments & Clinical History — Target Application

This repository defines the **target application** of the experiment:
the fixed specification the generator system receives (`SPEC.md`), the
hidden acceptance batteries (defined before the first run, never shown
to the generator), and the experiment runner.

Generated systems do not live here: each run builds in an isolated
workspace owned by the harness (`../glm/`), and the batteries run
against that workspace.

## Contents

- `SPEC.md` — fixed specification: 27 functional requirements, endpoint
  catalog (EP-01..EP-20), screens (SCR-01..SCR-08), deterministic seed,
  fixed stack (PostgreSQL 16 / NestJS / React / Vitest / Playwright /
  Docker Compose).
- `acceptance/` — hidden batteries (to be added; not part of what the
  generator ever sees).
- `runner/` — experiment runner (to be added).

## Why the stack is fixed

If each run chose its own stack, observed differences between
configurations C1/C2/C3 would be attributable to the chosen technology,
not to the engineering layers under study. A single language across
layers also keeps SonarQube/Semgrep measurements comparable.
