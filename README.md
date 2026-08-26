# AI Anti-Cheat API

Proof-of-concept API that explores how computer vision and large language models can assist with detecting visual indicators of unfair in-game advantages.

The project exposes a FastAPI endpoint that accepts a screenshot, validates the uploaded image, encodes it, combines it with example cheat/legitimate images and prompts, and sends the resulting multimodal request to an OpenAI vision model for analysis.

> This is an experimental project and is not intended to replace server-side anti-cheat systems, telemetry analysis, or other production security controls.

## Tech stack

- Python 3.11
- FastAPI
- OpenAI API
- Pydantic
- Poetry
- Uvicorn
- python-dotenv

## How it works

```text
Screenshot upload
      |
      v
FastAPI /api/v1/analyze
      |
      v
File validation + temporary storage
      |
      v
Image encoding
      |
      v
Prompt + reference examples
      |
      v
Vision model analysis
      |
      v
Parsed result
```

The API currently accepts `jpeg`, `jpg`, and `png` files.

## Project structure

```text
.
├── app.py
├── routers/
│   └── analyze.py
├── training_data/
├── pyproject.toml
├── poetry.lock
└── README.md
```

## Setup

### 1. Install dependencies

```bash
poetry install
```

### 2. Activate the Poetry environment

```bash
poetry shell
```

### 3. Configure your OpenAI API key

Linux/macOS:

```bash
export OPENAI_API_KEY="your-api-key"
```

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="your-api-key"
```

You can also use a local `.env` file because the application loads environment variables with `python-dotenv`.

### 4. Run the API

```bash
uvicorn app:app --reload
```

By default, FastAPI will expose the application locally and provide interactive API documentation through its standard Swagger UI.

## API

### `GET /`

Basic application health/root endpoint.

### `POST /api/v1/analyze`

Uploads an image for analysis.

Supported extensions:

- `.jpeg`
- `.jpg`
- `.png`

Example with curl:

```bash
curl -X POST \
  -F "file=@screenshot.png" \
  http://127.0.0.1:8000/api/v1/analyze
```

## What this project demonstrates

- Building REST APIs with FastAPI
- Handling multipart file uploads
- Environment-based secret configuration
- Integrating external AI APIs
- Multimodal prompt construction
- Image preprocessing/encoding
- Separating API routing from application bootstrap code
- Dependency management with Poetry

## Current status

This repository is a proof of concept. Some dependencies and model identifiers were pinned for the original implementation and may require updating before production use.

Potential next improvements include automated tests, Docker support, structured logging, API authentication, rate limiting, model abstraction, updated OpenAI API integration, and CI with GitHub Actions.

## License

MIT
