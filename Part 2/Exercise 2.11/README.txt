A dynamic content management system for publishing youtube videos and blog post in a single page web application. 

Setup Dockerfile
1. Using ubuntu 20.04 image
2. Install requires dependencies (python 3.8, pipenv, django)
3. Copy project files to /usr/src/app
4. Run pipenv install django
5. Run pipenv shell

Setup PostgreSQL database 
1. Using image Postgres:13.2-alpine
2.Set variables:
      POSTGRES_DB: mydb
      POSTGRES_USER: myuser
      POSTGRES_PASSWORD: mypass

3. Mount volume database:/var/lib/postgresql/data

Start django server using port 8000
python3 manage.py runserver

Visit http://127.0.0.1:8000/ in a web browser.You will see the following blank webpage without any contents

Now in web browser visit http://127.0.0.1:8000/admin . Login with the superuser name and password ( username: admin, pass: 12345)