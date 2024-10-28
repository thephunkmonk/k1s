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

# LOAD BALANCING
```bash
# Build a blog and a load balaner
$ docker build -t lb docker/nginx
$ docker build -t blog docker/httpd

# Run two (or more blogs) and the LB
$ docker run -d --name blog-1 --rm blog
$ docker run -d --name blog-2 --rm blog
$ docker run -d --name nginx_lb --link blog-1 --link blog-2 lb

# Checking if it works:
# Open logs for each blog and try curling localhost:8949 to see if everythings okay.

$ docker logs -f blog-1
$ docker logs -f blog-2
$ curl https://localhost:8949

```
