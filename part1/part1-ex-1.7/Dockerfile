FROM ubuntu

WORKDIR /app
RUN apt-get update && apt-get install -y curl

COPY . .
RUN chmod +x ./script

CMD ./script