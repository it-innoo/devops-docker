FROM node

COPY . /app
WORKDIR /app/frontend-example-docker-master/

RUN npm install
EXPOSE 5000
CMD ["npm","start"]