# IS 601 Module 11 - FastAPI Calculator

This repo is my Module 11 submission for IS 601.  
The goal of this module was to work with the application’s database/model layer, validation, testing, and CI/CD setup before moving further into the next module.

This project includes:
- a FastAPI calculator app
- SQLAlchemy models
- Pydantic schemas
- unit, integration, and E2E tests
- Docker + Docker Compose setup
- GitHub Actions CI/CD
- Docker Hub deployment

## What this project does

This app supports basic calculator operations like:
- addition
- subtraction
- multiplication
- division

For Module 11, the main focus was on:
- working with the calculation model
- validating calculation data with Pydantic
- testing calculator functionality
- keeping CI/CD working with PostgreSQL, Docker, and GitHub Actions

## Tech stack

- Python 3.10+
- FastAPI
- SQLAlchemy
- Pydantic
- PostgreSQL
- Playwright
- Pytest
- Docker / Docker Compose
- GitHub Actions

## Project structure

```bash
.
├── app/
│   ├── core/
│   ├── models/
│   ├── schemas/
│   ├── operations/
│   └── database.py
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── .github/
│   └── workflows/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── main.py