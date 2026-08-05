# DevSecOps Security Pipeline

A portfolio project demonstrating a modern DevSecOps CI/CD pipeline for a Python Flask application. This project integrates automated security testing, containerization, and software supply chain security into a GitHub Actions workflow.

---

## Features

- Flask web application
- Docker containerization
- Automated GitHub Actions CI/CD pipeline
- Static Application Security Testing (SAST)
- Container vulnerability scanning
- Software Bill of Materials (SBOM) generation

---

## Technology Stack

- Python 3.12
- Flask
- Docker
- GitHub Actions
- Bandit
- Semgrep
- Trivy
- Syft

---

## Project Structure

```
DevSecOps-Security-Pipeline/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── app/
│   ├── templates/
│   ├── app.py
│   └── requirements.txt
│
├── Dockerfile
├── .gitignore
└── README.md
```

---

## CI/CD Pipeline

Every push to the `main` branch automatically performs the following:

1. Checks out the repository
2. Sets up Python
3. Installs project dependencies
4. Verifies the Flask application
5. Runs Bandit security analysis
6. Runs Semgrep static analysis
7. Builds the Docker image
8. Performs a Trivy vulnerability scan
9. Generates a Software Bill of Materials (SBOM) using Syft

---

## Security Tools

| Tool | Purpose |
|------|---------|
| Bandit | Python security analysis |
| Semgrep | Static application security testing |
| Trivy | Container vulnerability scanning |
| Syft | Software Bill of Materials (SBOM) generation |

---

## Running Locally

Clone the repository:

```bash
git clone https://github.com/JulianBrito202/DevSecOps-Security-Pipeline.git
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

### Windows

```powershell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r app/requirements.txt
```

Run the application:

```bash
python app/app.py
```

Open:

```
http://localhost:5000
```

---

## Running with Docker

Build the image:

```bash
docker build -t devsecops-security-pipeline .
```

Run the container:

```bash
docker run -d -p 5000:5000 devsecops-security-pipeline
```

---

## Future Improvements

- Kubernetes deployment
- Infrastructure as Code (Terraform)
- Secret scanning
- Dependency update automation
- OWASP ZAP dynamic security testing

---

## Skills Demonstrated

- DevSecOps
- CI/CD
- Docker
- Secure Software Development
- GitHub Actions
- Static Application Security Testing
- Container Security
- Software Supply Chain Security

---

## License

This project is licensed under the MIT License.