FROM alpine
ENV project=devops
WORKDIR /opt/
RUN yum install httpd -y
COPY index.html var/www/html/index.html 
EXPOSE 80
CMD [ "httpd -D FOREGROUND" ]

FROM alpine:latest

# Insttall apache http server
RUN apk update && apk add --no-cache apache 2


# set environmanet variable
ENV project=devops

# set working directore
WORKDIR /var/www/localhost/htdocs/

# copy index.html to apache's working directory
COPY index.html  .

# expose port 80
EXPOSE 80

# start apache inforeground
CMD [ "/usr/bin/httpd", "-D", "FOREGROUND" ]