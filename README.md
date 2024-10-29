# K1S
- https://hub.docker.com/_/httpd

# BUILD & RUN
```bash

# BUILD 
$ docker build -t my-apache2 docker/httpd

# RUN
$ docker run -dit --name my-running-app -p 8949:80 my-apache2

# Get into the container
$ docker exec -it my-running-app bash

# Run & Execute container with access to current directory
$ docker run -dit --name my-running-app -p 8949:80 -v "$PWD":/usr/local/apache2/htdocs my-apache2
```

# Using Docker Compose
```
$ docker-compose up

# Follow the same steps as above

$ docker compose -f docker-compose.yaml up -d 
$ docker compose up -d 
$ docker compose up -d --build
$ docker compose up -d --build --force-recreate
$ docker compose up -d --scale blog=1
$ docker compose up -d --scale blog=2
$ docker compose up -d --watch

$ docker compose stop
$ docker compose start
$ docker compose down
```
