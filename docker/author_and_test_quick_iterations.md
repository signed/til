# Author and test a Dockerfile in quick iterations

```shell
docker run --rm -it $(docker build --file scratch.docker -q .) /bin/sh
```


## [How to unset ENTRYPOINT of a parent image](https://stackoverflow.com/questions/41207522/docker-override-or-remove-entrypoint-from-a-base-image)

```dockerfile
ENTRYPOINT ["/usr/bin/env"]
```
