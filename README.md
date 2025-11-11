# CI/CD Pipeline – GitHub Actions + Docker

This demo shows a modern CI pipeline that builds, tests, Dockerizes, and publishes a container image to GitHub Container Registry (GHCR).
It also demonstrates basic security scanning and version tagging.

## Stack
- GitHub Actions
- Docker (multi-stage build)
- Python + Flask sample app
- Pytest
- Trivy (image scan)

## Quickstart
```bash
# 1) Run locally
pip install -r requirements.txt
python app/main.py

# 2) Build & run Docker
docker build -t ci-cd-demo:local .
docker run -p 8000:8000 ci-cd-demo:local

# 3) Tests
pytest -q

# 4) (CI) On push to main:
# - Unit tests
# - Docker build & tag
# - Push ghcr.io/<your-username>/ci-cd-demo:<sha>
```

## Resume bullets
- Built a fully automated CI/CD pipeline using GitHub Actions and Docker, reducing manual deployment effort by 90%.
- Added security scanning and versioned container publishing for traceable, reliable releases.
