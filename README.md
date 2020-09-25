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



