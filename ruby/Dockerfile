FROM ruby:3.2.2-alpine3.18

RUN apk update
RUN apk add --no-cache build-base

COPY . /app
WORKDIR /app
RUN bundle install

ENTRYPOINT ["ruby"]
CMD ["server.rb"]
