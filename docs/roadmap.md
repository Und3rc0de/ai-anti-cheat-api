# Modernization roadmap

## Phase 1 — Make the current PoC reproducible

- Confirm supported Python version.
- Refresh dependency pins.
- Replace deprecated model/API usage.
- Add deterministic local configuration via `.env.example`.

## Phase 2 — Improve API design

- Introduce configuration/settings objects.
- Separate model-provider code from route handlers.
- Add request size and MIME validation.
- Normalize application errors and response schemas.
- Add `/health` and readiness endpoints.

## Phase 3 — Quality

- Add unit tests for parsing and validation.
- Add FastAPI endpoint tests.
- Add linting/type checks.
- Add GitHub Actions CI.

## Phase 4 — Deployment

- Add a production-oriented Dockerfile.
- Add Docker Compose for local development.
- Add structured logging and request IDs.
- Add authentication and rate limiting.

## Phase 5 — Evaluation

- Build a small labeled evaluation dataset.
- Track false positives/false negatives.
- Separate heuristic signals from model-assisted analysis.
- Document limitations and responsible-use constraints.
