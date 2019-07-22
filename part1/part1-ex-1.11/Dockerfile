FROM node

# Create app directory
COPY . /app
WORKDIR /app/backend-example-docker-master/

# Install app dependencies
RUN npm install

# ENV FRONT_URL=http://localhost:5000
EXPOSE 8000

CMD [ "npm", "start" ]