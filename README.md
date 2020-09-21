# Ready-To-Deploy Django, gunicorn, NGINX, Docker Application
Getting a Django 3.1 app up in no time. In this project, gunicorn is used as a WSGI. NGINX is used as a reverse proxy server.

## Credit
This repository is modified from the code created by [Watt Iamsuri](https://github.com/wiamsuri/django-gunicorn-nginx-docker).

## Getting Started
For Ubuntu (remember to login/logout after running command)
```
sudo curl -sSL https://get.docker.com/ | sh
sudo usermod -a -G docker $(whoami)
sudo service docker start
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

In the root level of this repository, copy the file named `django.env.example` to `django.env` and adjust file variables

```
cp django.env.example django.env
```

Build code with docker compose
```
docker-compose build
```

Run the built container
```
docker-compose up -d
```
