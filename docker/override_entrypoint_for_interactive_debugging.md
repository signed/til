# Override entrypoint for interactive debugging

in the compose file add this to the service

```
services:
  service:
    stdin_open: true        # docker run -i 
    tty: true               # docker run -t 
    entrypoint: ["/bin/sh"] # run shell instead of the default entrypoint
```
Then execute `docker compose up -it service` into a shell inside the container.
