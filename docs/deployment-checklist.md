# Deployment checklist

- [ ] Replace deprecated model/API usage.
- [ ] Pin and audit dependencies.
- [ ] Configure secrets outside source control.
- [ ] Add upload size and MIME validation.
- [ ] Add authentication if exposed beyond a trusted environment.
- [ ] Add rate limiting and abuse controls.
- [ ] Use structured logging without secrets or uploaded image contents.
- [ ] Run automated tests in CI.
- [ ] Build and scan the container image when Docker support is added.
- [ ] Document model limitations and human-review requirements.
