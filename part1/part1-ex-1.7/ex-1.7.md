# Part1
## Excercise 1.7

### script file
```
echo "Input website:";
read website; echo "Searching..";
sleep 1;
curl http://$website;

```

### Dockerfile
```
FROM ubuntu

WORKDIR /app
RUN apt-get update && apt-get install -y curl

COPY . .
RUN chmod +x ./script

CMD ./script
```

### Commands
```
$ docker build --t=curler .
$ docker run --rm -it curler

```

### Output
```
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```
