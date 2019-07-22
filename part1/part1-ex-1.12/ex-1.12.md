# Part1
## Excercise 1.12

### frontend Dockerfile
```
FROM node

COPY . /app
WORKDIR /app/frontend-example-docker-master/

RUN npm install

ENV API_URL=http://localhost:8000
EXPOSE 5000
CMD ["npm","start"]
```

### backend Dockerfile
```
FROM node

# Create app directory
COPY . /app
WORKDIR /app/backend-example-docker-master/

# Install app dependencies
RUN npm install

ENV FRONT_URL=http://localhost:5000
EXPOSE 8000

CMD [ "npm", "start" ]
```

### commands
```
$ docker run -p 5000:5000 frontend
$ docker run -v $(pwd)/backend-example-docker-master/logs.txt:/app/backend-example-docker-master/logs.txt -p 8000:8000 backend
```
