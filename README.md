
# Customer Accounts Microservice

A RESTful Customer Accounts Microservice developed as part of the IBM DevOps and Software Engineering Capstone Project.

[![Build Status](https://github.com/Abhi-Uphade/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/Abhi-Uphade/devops-capstone-project/actions/workflows/ci-build.yaml)

## Project Overview

The project focuses on developing a Flask-based REST API for managing customer accounts and applying DevOps practices throughout the software development lifecycle.

### Features

- Create customer accounts
- Retrieve an individual account
- List all accounts
- Update customer account information
- Delete customer accounts
- Validate API requests
- Handle application errors
- Apply security headers and CORS policies

## Technology Stack

- Python
- Flask
- SQLAlchemy
- PostgreSQL
- Git and GitHub
- Docker
- GitHub Actions
- Nose
- Flake8
- Kubernetes
- Tekton

## Repository Structure

```text
.
├── service/          # Flask application and REST API
├── tests/            # Automated tests
├── deploy/           # Deployment configuration
├── tekton/           # Tekton pipeline resources
├── .github/
│   └── workflows/    # GitHub Actions workflows
├── Dockerfile
├── Makefile
├── requirements.txt
└── setup.cfg
```

## Local Test Results

The restored application has been tested locally.

| Check | Result |
|---|---:|
| Automated tests | 34 passed |
| Test failures | 0 |
| Overall test coverage | 96% |
| Critical Flake8 checks | 0 errors |
| Flake8 style checks | 0 violations |

These results are from local testing. GitHub Actions CI execution will be documented after verification.

## Development Setup

### 1. Clone the repository

```bash
git clone https://github.com/Abhi-Uphade/devops-capstone-project.git
cd devops-capstone-project
```

### 2. Create a virtual environment

```bash
python3 -m venv ~/venv
source ~/venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start PostgreSQL

```bash
docker run -d \
  --name postgresql \
  -p 5432:5432 \
  -e POSTGRES_PASSWORD=postgres \
  -v postgresql:/var/lib/postgresql/data \
  postgres:alpine
```

### 5. Run tests

```bash
nosetests -v
```

### 6. Run lint checks

```bash
flake8 service --count --select=E9,F63,F7,F82 --show-source --statistics

flake8 service --count --max-complexity=10 --max-line-length=127 --statistics
```

## Project Progress

- [x] Restore application source and test environment
- [x] Verify account model tests
- [x] Verify REST API tests
- [x] Verify CLI and error-handler tests
- [x] Run complete test suite
- [x] Run local Flake8 checks
- [ ] Verify GitHub Actions CI
- [ ] Complete remaining security and DevOps tasks
- [ ] Verify Docker and Kubernetes deployment
- [ ] Complete Tekton continuous delivery pipeline

## Source Attribution

This academic project is based on the IBM DevOps and Software Engineering Capstone.

The restored application source includes material from the following reference repository:

https://github.com/christian-schw/devops-capstone-project

The reference implementation is acknowledged here. Further modifications, testing, configuration, and project work will be documented as they are completed.
