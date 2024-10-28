# K1S
- https://hub.docker.com/_/httpd

# BUILD & RUN
```bash
$ docker build -t my-apache2 .
$ docker run -dit --name -my-running-app -p 8949:80 my-apache2
$ docker exec -it my-apache2 bash
