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

```
