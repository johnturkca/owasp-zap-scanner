# OWASP ZAP Web App Security Scanner

Automated web application security scanning pipeline using **OWASP ZAP** to detect OWASP Top 10 vulnerabilities, integrated into CI/CD for continuous security validation.

## Features
- Automated active & passive scanning via OWASP ZAP
- Detects SQL Injection, XSS, CSRF, and other OWASP Top 10 vulnerabilities
- Docker-based isolated test environment
- CI/CD pipeline integration (GitLab CI / GitHub Actions)
- HTML and JSON report generation

## Tech Stack
`Python` `OWASP ZAP` `Docker` `CI/CD` `Bash`

## Run with Docker
```bash
docker-compose -f docker-compose.yml up --build -d
```
To view reports, navigate to `reports/`

## Run Locally
```bash
# Start ZAP daemon
docker-compose up -d owaspzap

# Install dependencies
pip3 install -r requirements.txt

# Run scan
python3 zap_scanner.py --target https://your-target.com
```

## Disclaimer
This tool is intended for authorized security testing only. Always obtain proper written permission before scanning any target.
