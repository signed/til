# Keep your environment clean


## Remove all stopped containers
````shell
docker rm $(docker ps -a | grep Exited | awk '{print $1}')
````

## Clean up un-tagged docker images
````shell
docker rmi $(docker images -q --filter "dangling=true")
````

## Stop and remove all containers (including running containers)
````shell
docker rm -f $(docker ps -a -q)
````

