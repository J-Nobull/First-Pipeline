# Python Test App – First Deployment

This repository contains a simple Python application that demonstrates automated deployment using 
  **GitHub Actions** and **Heroku**. It was created as a learning exercise for understanding 
  CI/CD pipelines and cloud deployment.

## What This Project Does
- Installs Python dependencies
- Lints code with `flake8`
- Runs tests using `pytest`
- Deploys to Heroku automatically on every push to the `main` branch

## Deployment Pipeline

This project uses a GitHub Actions workflow defined in `.github/workflows/python-app.yml`. 
Here's what it does:
1. **Checks out the code**
2. **Sets up Python** (original build on Python 3.12 via Heroku’s `.python-version` file)
3. **Installs dependencies** from `requirements.txt`
4. **Lints** the code using `flake8`
5. **Runs tests** using `pytest`
6. **Deploys to Heroku** if the push is to the `main` branch

## Requirements

- `requirements.txt` in the root directory with your dependencies
- `.python-version` file to specify your Heroku Python runtime
- `Procfile` in the root directory to declare the process type (e.g., `web: python app.py`)
- GitHub repository secrets:
  - `HEROKU_TOKEN`: your Heroku API key
  - `HEROKU_APP_NAME`: your Heroku app name

## File Overview

- `.github/workflows/python-app.yml` – GitHub Actions workflow
- `Procfile` – tells Heroku how to run your app
- `.python-version` – specifies Python version for Heroku
- `requirements.txt` – Python dependencies
- `app.py` – your main application file
- `README.md` – you're reading it!

## Notes

- This was my **first attempt** at deploying a Python app using CI/CD. 

## Resources

- [Heroku Python Support Docs](https://devcenter.heroku.com/articles/python-support)
- [GitHub Actions for Python](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python)
