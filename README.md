# recipe-app-api
Recipe app api source code

# Command to test
docker-compose run app sh -c "python manage.py test && flake8"

# build 
docker-compose build

# Create core app
docker-compose run app sh -c "python manage.py startapp core"
docker-compose run --rm app sh -c "python manage.py startapp user"

# make migrations
docker-compose run app sh -c "python manage.py makemigrations core"

# Run 
docker-compose up