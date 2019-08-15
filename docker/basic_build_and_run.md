# Basic build and run

````shell
echo 'FROM node:12.8.0-alpine' > Dockerfile
docker build -t <your username>/<image name> .
docker run --entrypoint "sh" -it <your username>/<image name>
````
