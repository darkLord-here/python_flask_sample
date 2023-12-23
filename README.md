# Steps to run the projects
- install poetry <code>pip install poetry</code>
- <code>poetry init</code> initialize the poetry
- <code>poetry install</code> installs the dependencies
- <code>poetry run flask --app best_practices init_db</code> intializes the database
- <code>poetry run waitress-serve --call best_practices:create_app</code> Run the code in production


# Steps followed
- ```pip install poetry```
- ```poetry new best_practices```
- Develop the codebase
- ```poetry add flask```
- ```poetry add waitress```
- ```poetry add pytest -D```
- ```poetry add pre-commit -D```
- ```git init```
- ```poetry run pre-commit sample-config > .pre-commit-config.yaml```
- Added the following code in ```.pre-commit-config.yaml``` <br>
```
-   repo: local
    hooks:
    -   id: check-required-files
        name: Check for required files
        entry: python -c "import os; assert os.path.isfile('.gitignore'), '.gitignore is missing'"
        language: system
        pass_filenames: false
```
- ```git add```
- ```poetry run pre-commit install```
