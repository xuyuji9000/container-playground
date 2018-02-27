
# Init a Django project

1. create virtual environment: `virtualenv -p python3 venv`

2. activate environment: `source ./venv/bin/activate`

3. install dependency: `pip3 install -r requirements.txt`

4. init Django project: `django-admin startproject helloworld`

5. create start.sh for initing app, and `sudo chmod +x ./start.sh`

# Setup Local Dockerized Environment

1. build docker image: `docker build -t django-ecs .`

2. run docker instance: `docker run -it -p 8000:8000 --rm --name django-ecs django-ecs`

# Push Image to ECR(Elastic Container Registery)

1. get ecr login info: `aws ecr get-login --no-include-email --region ap-northeast-2 && login`

2. build image: `docker build -t django-ecs .`

3. tag with ecr info: `docker tag django-ecs:latest $(aws sts get-caller-identity --query "Account" --output text).dkr.ecr.ap-northeast-2.amazonaws.com/django-ecs:latest`


4. push to ECR: `docker push $(aws sts get-caller-identity --query "Account" --output text).dkr.ecr.ap-northeast-2.amazonaws.com/django-ecs:latest`

# Reference

- [Dockerizing a Python Django Web Application](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application)
