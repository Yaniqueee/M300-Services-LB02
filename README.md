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

### Netzwerkplan

### Testing

![image](https://user-images.githubusercontent.com/78543849/114039816-5a6a8480-9883-11eb-86bd-d05e0a1b303d.png)


