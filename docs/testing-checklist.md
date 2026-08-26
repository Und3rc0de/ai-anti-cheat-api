# Testing checklist

- [ ] Root endpoint returns a successful response.
- [ ] Analyze endpoint accepts JPEG/JPG/PNG files.
- [ ] Unsupported extensions return HTTP 400.
- [ ] Empty or malformed uploads are rejected safely.
- [ ] API key configuration errors return controlled responses.
- [ ] Temporary files are cleaned up after processing.
- [ ] Provider failures are translated into stable API errors.
- [ ] Response parsing is covered by unit tests.
- [ ] File-size limits are enforced before public deployment.
- [ ] CI runs tests on supported Python versions.
