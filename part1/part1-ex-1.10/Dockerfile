FROM node

COPY . /app
WORKDIR /app/frontend-example-docker-master/

RUN npm install

ENV API_URL=http://localhost:8000
EXPOSE 5000
CMD ["npm","start"]