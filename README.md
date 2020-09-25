# Dockersfiles
git clone https://gitlab.com/qacdevops/trio-task.git
cd trio-task
cd Dockerfile

vim Dockerfile

#use python image
FROM python:3.7

#Install apt depedencies

#copy  content of image
COPY . .

#Run pip dependencies
Run pip install flask

#Expose the correct port
EXPOSE 5000

#create an entrypoint 
ENTRYPOINT [ "python", "app.py"]


Sudo docker build -t trio-task .

Sudo docker run -d -p 5000: 5000 --trio-task trio-task

sudo docker stop trio-task

sudo docker rm trio-task

sudo docker rmi trio-task

MySQL

Vim into Docker
FROM mysql:5:7

ENV MYSQL_DATABASE=flask-db

RUN pip install flask flask_sqlalchemy pymysql

export FLASK_DB_PASSWORD=winter

sudo docker run --env MYSQL_ROOT_PASSWORD=$flask_db -d -p 3306:3306 --name mysql

touch nginx .conf

vim nginx .conf

events {}
http {
    server {
        listen 80;
        location / {
            proxy_pass http://server:5000;
        }
    }
}





