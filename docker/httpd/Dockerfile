FROM httpd:2.4
COPY ./my-httpd.conf /usr/local/apache2/conf/httpd.conf
#build an argument
ARG REPO_URL='https://github.com/thephunkmonk/k1s.git'

#same as RUN apt-get update
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "vim"]
RUN ["apt-get", "install", "-y", "git"]
#RUN ["git", "clone", ${REPO_URL}, "/usr/local/apache2/blog"]
RUN git clone ${REPO_URL} /usr/local/apache2/blog

# docker run -> <>.github.io
