#---------------------------------------------------------------------------
# Dockefile to build Docker Image of Apache WebServer
#
# Created by Nikolai Tugov
#---------------------------------------------------------------------------

FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y apache2
RUN echo 'Hello world from Docker!' > /var/www/html/index.html

CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]
EXPOSE 80
