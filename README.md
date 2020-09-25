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

RUN
