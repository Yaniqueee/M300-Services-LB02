# M300-Services LB02 Docker

## Docker Commands

#### Docker Testen

```Shell
      $  docker run hello-world
```

#### Docker Container mit Shell starten


```Shell
      $  docker run -it ubuntu /bin/bash
```

#### Aktive (und beendete) Container anzeigen

```Shell
      $  docker ps (-a)
```

#### Docker Images anzeigen

```Shell
      $  docker image ls
```

#### Mit Docker ein File vom Host zu einem Container kopieren

```Shell
      $  docker cp /SpeicherortDerDatei/index.html ContainereName:/var/www/html/
```

## Docker Web Umgebungs Dokumentation 

### Konfiguration

* Betriebssystem: Ubuntu:14.04
* Imagename: Webserver
* Programme: Apache2
* Port Weiterleitung: 80

### Dockerfile zur erstellung des Containers

```Shell
#
#	Einfache Apache Umgebung
#
FROM ubuntu:14.04
MAINTAINER Marcel mc-b Bernet <marcel.bernet@ch-open.ch>

RUN apt-get update
RUN apt-get -q -y install apache2 

# Konfiguration Apache
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

RUN mkdir -p /var/lock/apache2 /var/run/apache2

EXPOSE 80

VOLUME /var/www/html

CMD /bin/bash -c "source /etc/apache2/envvars && exec /usr/sbin/apache2 -DFOREGROUND"
```

### Netzwerkplan

![image](https://user-images.githubusercontent.com/78543849/114041211-9fdb8180-9884-11eb-94e3-ce224f30bcf7.png)

### Testing

![image](https://user-images.githubusercontent.com/78543849/114039816-5a6a8480-9883-11eb-86bd-d05e0a1b303d.png)


