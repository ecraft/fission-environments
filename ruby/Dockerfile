FROM ruby:3.2.2-alpine3.18

RUN apk update
RUN apk add --no-cache build-base libpq

WORKDIR /app
COPY Gemfile Gemfile.lock server.rb /app
COPY fission /app/fission
RUN bundle install

ENTRYPOINT ["ruby"]
CMD ["server.rb"]
