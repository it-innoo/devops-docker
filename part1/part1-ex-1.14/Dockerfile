FROM ruby:2.6.0

ADD . /app
WORKDIR /app/rails-example-project-master/

RUN apt-get update && apt-get install -y nodejs
RUN bundle install
RUN gem install execjs
RUN rails db:migrate

EXPOSE 3000
CMD [ "rails", "s" ]