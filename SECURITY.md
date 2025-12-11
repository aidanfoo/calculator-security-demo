# Security Scanning

## Overview
This repository uses three types of security scanning:

### SAST (Static Analysis with CodeQL)
- Scans source code for vulnerabilities
- Runs on push to main branch
- Checks for: [Logic flaws, Unsafe coding patterns, Data flow vulnerabilities, Missing input validation]
- Artifacts: See GitHub Security tab
Workflow: .github/workflows/1-sast-only.yml

### SCA (Dependency Check)
- Scans Python packages for known CVEs
- Runs on push to main branch
- Checks for: [Outdated libraries, Known CVEs in dependencies, Vulnerable or unmaintained packages]
- Artifacts: sca-reports
- .github/workflows/2-sca-only.yml

### DAST (Live Application with ZAP)
- Tests running application for vulnerabilities
- Runs on push to main branch
- Checks for: [Missing or weak security headers, Runtime misconfigurations, Exposed or vulnerable endpoints, Injection vulnerabilities observable at runtime]
- Artifacts: zap-baseline-reports, zap-fullscan-reports
- Workflow: .github/workflows/dast-only.yml

## Understanding Results
[Link to Part 10 in README]

## Reporting Vulnerabilities
Please email security@example.com