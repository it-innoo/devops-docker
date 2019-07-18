# Part1
## Excercise 1.1
### Initial
```
$docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

```

### Start 3 containers
```
$ docker run -d nginx
$ docker ps -a

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
0342a9ebb62f        nginx               "nginx -g 'daemon of…"   8 seconds ago       Up 5 seconds        80/tcp              nifty_kepler
b53ce92d22d3        nginx               "nginx -g 'daemon of…"   53 seconds ago      Up 47 seconds       80/tcp              romantic_benz
b8324aec32e5        nginx               "nginx -g 'daemon of…"   2 hours ago         Up 2 hours          80/tcp              blissful_noyce
```
### Stop 2 of the containers leaving 1 up.
```
$ docker stop b8324aec32e5

$ docker stop b53

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                          PORTS               NAMES
0342a9ebb62f        nginx               "nginx -g 'daemon of…"   25 minutes ago      Up 25 minutes                   80/tcp              nifty_kepler
b53ce92d22d3        nginx               "nginx -g 'daemon of…"   26 minutes ago      Exited (0) 7 seconds ago                            romantic_benz
b8324aec32e5        nginx               "nginx -g 'daemon of…"   2 hours ago         Exited (0) About a minute ago
```

## Excercise 1.2

### Initial
```
$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               latest              f68d6e55e065        2 weeks ago         109MB

$ docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                     PORTS               NAMES
0342a9ebb62f        nginx               "nginx -g 'daemon of…"   21 hours ago        Exited (0) 8 minutes ago                       nifty_kepler
b53ce92d22d3        nginx               "nginx -g 'daemon of…"   21 hours ago        Exited (0) 20 hours ago                        romantic_benz
b8324aec32e5        nginx               "nginx -g 'daemon of…"   22 hours ago        Exited (0) 20 hours ago                        blissful_noyce
```

### Clean the docker daemon from all images and containers.

```
$ docker rm b8324
$ docker rm b53ce
$ docker rm 0342
```
```
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
$ docker rmi f68d
Untagged: nginx:latest
Untagged: nginx@sha256:48cbeee0cb0a3b5e885e36222f969e0a2f41819a68e07aeb6631ca7cb356fed1
Deleted: sha256:f68d6e55e06520f152403e6d96d0de5c9790a89b4cfc99f4626f68146fa1dbdc
Deleted: sha256:1b0c768769e2bb66e74a205317ba531473781a78b77feef8ea6fd7be7f4044e1
Deleted: sha256:34138fb60020a180e512485fb96fd42e286fb0d86cf1fa2506b11ff6b945b03f
Deleted: sha256:cf5b3c6798f77b1f78bf4e297b27cfa5b6caa982f04caeb5de7d13c255fd7a1e

$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```