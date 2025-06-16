# SBOM in a CI/CD Pipeline Demo

This repository demonstrates how to integrate Software Bill of Materials (SBOM) generation and vulnerability scanning into a CI/CD pipeline using GitHub Actions, Syft, and Grype.

## Project Structure

```
myapp/
├── Dockerfile
├── app.py
├── requirements.txt
└── .github/workflows/sbom.yml
```

## Workflow Overview

The GitHub Actions workflow (`.github/workflows/sbom.yml`) performs the following steps:

1. **Build Docker image** for the sample Flask app.
2. **Generate SBOM** using Syft in CycloneDX JSON format.
3. **Store SBOM as an artifact** for later review or compliance.
4. **Scan SBOM for vulnerabilities** using Grype.

## How to Use

1. **Clone this repository** and navigate to the `myapp` directory.
2. **Push any change** to trigger the workflow.
3. **View workflow results** in the GitHub Actions tab, including the generated SBOM and vulnerability scan results.

## Sample Application

The sample app is a minimal Flask web server (`app.py`).

## Requirements

- Docker
- GitHub Actions (runs automatically on push)

## References
- [Syft Documentation](https://github.com/anchore/syft)
- [Grype Documentation](https://github.com/anchore/grype)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

---

Feel free to modify the app or workflow to fit your own use case!
