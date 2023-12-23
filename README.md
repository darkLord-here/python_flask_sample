# Steps to run the projects
- install poetry <code>pip install poetry</code>
- <code>poetry init</code> initialize the poetry
- <code>poetry install</code> installs the dependencies
- <code>poetry run flask --app best_practices init_db</code> intializes the database
- <code>poetry run waitress-serve --call best_practices:create_app</code> Run the code in production
