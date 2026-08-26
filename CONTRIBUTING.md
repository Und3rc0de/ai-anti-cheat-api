# Contributing

This repository is currently maintained as an experimental proof of concept.

## Development workflow

1. Fork or clone the repository.
2. Create a feature branch from `main`.
3. Keep changes focused and document behavioral changes.
4. Add or update tests when application behavior changes.
5. Open a pull request describing the problem, the approach, and how the change was validated.

## Local development

```bash
poetry install
poetry shell
uvicorn app:app --reload
```

Set `OPENAI_API_KEY` in your environment or copy `.env.example` to `.env` and provide your own key.

## Suggested areas for improvement

- Update the OpenAI integration and model configuration.
- Add unit and API tests with pytest.
- Add Docker support.
- Add structured logging and error handling.
- Add authentication and rate limiting before any public deployment.
- Add CI for linting and tests.
