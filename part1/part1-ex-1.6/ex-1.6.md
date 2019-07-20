# Part1
## Excercise 1.6

### Dockerfile
```
FROM devopsdockeruh/overwrite_cmd_exercise

CMD ["-c"]
```

### Commands
```
$ docker build --t=docker-clock .
docker run --rm -it docker-clock:latest
```
