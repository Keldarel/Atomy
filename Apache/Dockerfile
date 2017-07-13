FROM ubuntu

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
    && apt-get install --allow-unauthenticated -y --no-install-recommends apache2 libapache2-mod-jk vim net-tools

ADD apache_startup.sh /etc/apache2/apache_startup.sh

VOLUME ["/var/log/apache2"]

EXPOSE 80 443

ENTRYPOINT /etc/apache2/apache_startup.sh










