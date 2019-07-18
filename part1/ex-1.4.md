# Part1
## Excercise 1.4

```
$ docker pull devopsdockeruh/exec_bash_exercise
Using default tag: latest
latest: Pulling from devopsdockeruh/exec_bash_exercise
741437d97401: Pull complete 
34d8874714d7: Pull complete 
0a108aa26679: Pull complete 
7f0334c36886: Pull complete 
65c95cb8b3be: Pull complete 
a36b708560f8: Pull complete 
4090f912e6c7: Pull complete 
ce5fe2607c2e: Pull complete 
9400f5f657d6: Pull complete 
c4919883f7fa: Pull complete 
Digest: sha256:c463832132d1fb0b8b3b60348a6fc36fda7512a4ef2d1050e8bea7b6a6d7a2f3
Status: Downloaded newer image for devopsdockeruh/exec_bash_exercise:latest

$ docker run -d --name looper devopsdockeruh/exec_bash_exercise
18eea33d596f40d681f0ee82a11cd206291c9a6aea031b9ce670e95cb2762238

$ docker exec -it looper bash
root@18eea33d596f:/usr/app# tail -f ./logs.txt
Secret message is:
"Docker is easy"
```