

# Init a Django project

1. create virtual environment: `virutalenv -p python3 venv`

2. activate environment: `source ./venv/bin/activate`

3. install dependency: `pip3 install -r requirements.txt`

4. init Django project: `django-admin startproject helloworld`

# Setup Dockerized Environment

1. build docker image: `docker build -t python-backend .`

2. run docker instance: `docker run -it -p 8000:8000 --rm --name python-backend python-backend`
