# Architecture overview

```text
Client
  |
  | multipart image upload
  v
FastAPI
  |
  v
/api/v1/analyze
  |
  +--> extension validation
  |
  +--> temporary file
  |
  +--> image encoding
  |
  +--> reference examples + prompts
  |
  v
AI provider request
  |
  v
response parsing
  |
  v
API response
```

The current proof of concept keeps most orchestration inside the route handler. A future version should move provider calls, configuration, validation, and domain analysis into separate services so they can be tested independently.
