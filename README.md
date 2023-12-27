# Simple Notes App
This is a simple notes application built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/amar-m-cloud/django-notes-application.git
```

2. Build the app
```
docker build -t django-notes-application .
```

3. Run the app
```
docker run -d -p 8000:8000 django-notes-application:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`
