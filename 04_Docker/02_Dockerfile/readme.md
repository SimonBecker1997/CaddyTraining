# Creating a Caddy Docker image with a website and configs
## About this lab
This lab shows you on how to create a website that is hosted by caddy in a docker container.
The lab shows you on how to create the Dockerfile as well as how to build and start the container.

## Lab 1: Run the docker-compose.yml
1. To run the lab, clone this repository to your server
2. Then, navigate into this directory.
3. Change the domain in the caddyfile, so that it matches your domain (in case you do not have a domain, use localhost, works too)
4. Create a volume that is called  caddy_data: `docker volume create --name=caddy_data`
5. Run the docker-compose file, by typing into your command prompt:
```
docker-compose up
```
## Lab2: Build the Image and upload it
You can also upload your caddy image with website to dockerhub, so everyone can deploy it. 
Therfore log in to docker hub and create a repository.  
Then build the docker image by running: 
```
docker build -t yourdockeraccount/repositoryname:tag .
```
Then upload it by running: 
```
docker push yourdockeraccount/repositoryname:tag
```
You can use the image on docker hub: https://hub.docker.com/r/nobody1997/mywebsite
