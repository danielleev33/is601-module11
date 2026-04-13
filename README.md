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

How to clone the repo
git clone git@github.com:danielleev33/is601-module11.git
cd is601-module11
How to create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate
How to install dependencies
pip install --upgrade pip
pip install -r requirements.txt
python -m playwright install
How to run the app locally without Docker

If you want to run the FastAPI app directly:

uvicorn main:app --host 0.0.0.0 --port 8000 --reload

Then open:

http://localhost:8000
How to run the app with Docker

This is usually the easiest way once Docker is set up properly.

Build and start the containers
docker compose up --build

This starts:

the FastAPI app
PostgreSQL
pgAdmin
App URLs
FastAPI app: http://localhost:8000
pgAdmin: http://localhost:5050
Stop the containers
docker compose down
Full cleanup if needed
docker compose down -v

That also removes the volumes, which is useful if PostgreSQL decides to be difficult.

How to run the tests

This project includes three types of tests:

unit tests
integration tests
end-to-end (E2E) tests

Before running tests locally, make sure your virtual environment is activated:

source venv/bin/activate
Run all tests
pytest -v
Run only unit tests
pytest tests/unit -v
Run only integration tests
pytest tests/integration -v
Run only E2E tests
pytest tests/e2e -v
Notes about tests
Unit tests check the calculator operation logic.
Integration tests check the application logic, schemas, and database-related behavior.
E2E tests use Playwright to simulate user interaction in the browser.

If E2E tests are being run locally, make sure Playwright is installed:

python -m playwright install