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


