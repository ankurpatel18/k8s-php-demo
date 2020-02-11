# k8s-php-demo
Set up a PHP in docker and deploy using k8s in minikube.

##  prerequisite
minikube

kuberctl

docker

docker-compose

## Start Minikube
1) To create Build from Dockerfile you should in same level where Docker file located on my Repo.

    `minikube start`

2) setup docker enviroment for minukube 

    `eval $(minikube docker-env)`

## build and start docker conatiner
3) build and start docker container from root of project

    `docker-compose up -d --build`

## using kubectl
4) setup webserver pods using kubectl
    
    `kubectl create -f webserver.yaml`

5) setup webserver service using kubectl

    `kubectl create -f webserver-svc.yaml`

6) check on what port need to run my app

    `kubectl get svc`

    inside check for "web-service" and port look like 80:30203  so "30203" is yourport need to run in browser using http://localhost:30203
