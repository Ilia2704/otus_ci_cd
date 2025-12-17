# CI/CD for ML

This repository is a demo MLOps / CI-CD project created as part of an OTUS course.
It demonstrates a typical machine learning workflow with automated testing and CI:
data preparation, model training, validation, and application-level execution.

The focus is on reproducibility, code quality, and CI/CD practices rather than model complexity.

## Clone and Push to Your Own GitHub Repository

### Clone the original repository

### Change the remote to your own repository
```bash
git remote remove origin
git remote add origin https://github.com/Ilia2704/otus-cicd.git
```

### Verify the remote
```bash
git remote -v
```

#### You should see:
`origin  https://github.com/Ilia2704/otus-cicd.git (fetch)`

`origin  https://github.com/Ilia2704/otus-cicd.git (push)`

### Push your local branch
```bash
git push -u origin HEAD
```

#### Note:
When using HTTPS, GitHub will ask for your username and password.
Use your Personal Access Token (PAT) instead of the password.



## Create ENV 

```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements/requirements.txt
```

## Run the project
### Run tests
``` 
pytest -q
```

### Train the model

``` python -m src.train ```

### Run the application (if applicable)

``` python -m src.app ```

``` streamlit run src/app.py ```

## Project structure

```text
otus_ci_cd/
├── src/            # Application and ML logic
├── tests/          # Unit and integration tests
├── data/           # Training / demo data
├── models/         # Trained model artifacts
├── scripts/        # Helper and automation scripts
├── requirements/   # Dependency definitions
└── .github/        # CI/CD workflows
```

## CI/CD

This repository uses GitHub Actions for continuous integration:
- dependency installation
- automated tests
- basic validation of the training pipeline

CI configuration is located in .github/workflows/.

> **Note:** Deployment assumes a pre-existing target instance.
> The CI/CD pipeline will fail if the instance is not available.