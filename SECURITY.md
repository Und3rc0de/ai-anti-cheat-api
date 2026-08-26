# Security

## API keys

Never commit OpenAI API keys or other credentials to the repository. Use environment variables or a local `.env` file that is excluded from version control.

## File uploads

The current project is a proof of concept. Before exposing it publicly, add production-grade controls for upload size, MIME validation, malformed files, request timeouts, authentication, rate limiting, temporary-file cleanup, and abuse prevention.

## AI output

Model output should be treated as advisory. It must not be used as the sole basis for punitive action against a player or user.

## Reporting

If you discover a security issue, avoid publishing secrets or exploit details in a public issue. Contact the repository maintainer privately where possible.
