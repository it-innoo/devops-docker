# Part1
## Excercise 1.8

### Commands
```
$ touch logs.txt
$ docker run -d -v "$(pwd)"/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
```
###Output
```
Sun, 21 Jul 2019 10:36:53 GMT
Sun, 21 Jul 2019 10:36:56 GMT
Sun, 21 Jul 2019 10:36:59 GMT
Sun, 21 Jul 2019 10:37:02 GMT
Secret message is:
"Volume bind mount is easy"
Sun, 21 Jul 2019 10:37:08 GMT
Sun, 21 Jul 2019 10:37:11 GMT
Sun, 21 Jul 2019 10:37:14 GMT


```
