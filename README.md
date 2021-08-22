Install Docker:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html

EC2 --> Install docker --> Create containers --> install apps inside containers


$sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose  -->uses to create docker compose which uses to create containers using YAML manifests


$chmod +x /usr/local/bin/docker-compose --> Permission for docker-compose as executable:

Using Docker Compose YAML file created docker container:
docker-compose.yml:

version: '3'

services:
  jenkins:
    container_name: jenkins
    image: jenkins/jenkins:lts-jdk11
    ports:
      - "8080:8080"

$chmod +x /usr/local/bin/docker-compose --> Permission for docker-compose.yml as executable:

$docker-compose up -d -> Uses to create container from docker-compose.yml file

Docker commands:
$docker info --> uses to check the status of docker
$docker ps --> uses to see the running containers
$docker logs containername/id --> will show the particular container logs


