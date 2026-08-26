# Maintenance guidance

This proof of concept depends on fast-moving AI APIs and should be maintained with explicit compatibility checks.

When updating it:

1. Record the supported Python version.
2. Review OpenAI SDK/model deprecations.
3. Update and audit dependency pins.
4. Run API and parsing tests.
5. Validate file handling and temporary-file cleanup.
6. Re-run the evaluation dataset when model behavior changes.
7. Update the README/changelog with compatibility notes.

Keep provider-specific behavior behind a narrow interface so future API changes do not require rewriting route handlers.
