# rancher-compose-helloworld
This repository demos how to use rancher-compose to create a hello world container.
the docker image that be used in this demo is from https://hub.docker.com/r/kitematic/hello-world-nginx

## Option 1 - Use Docker Remote API in docker-compose.yml
In this link https://forums.rancher.com/t/rancher-compose-and-local-dockerfile-using-build/612 it describes how to use Docker Remote API in docker-compose and rancher-compose to create a container. This demo doesn't go with this solution.
TODO - A seperate demo will be created and go with this solution.

## Option 2 - use image parameter in docker-compose.yml
This demo goes with this solution

## How do I
1) Clone this repository
2) in bash console, cd to the repository folder
3) run ```rancher-compose --debug up -d```
* --debug is used for display debug information in bash console
* -d runs the container in detached mode. Go to https://docs.docker.com/compose/reference/up/ to find more detail.

## Learned things
* If ```rancher-compose up``` is run successfully, rancher will create a service for you, named 'helloworld'. Then I tried change the local docker-compose file and the change didn't influence the subsequnt ```rancher-compose up``` command. You need to run ```rancher-compose rm helloworld``` to remove the existing service, and then your local docker-compose.yml will be used by rancher again.
