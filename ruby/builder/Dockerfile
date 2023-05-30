ARG BUILDER_IMAGE=fission/builder:latest
FROM ${BUILDER_IMAGE}

FROM ruby:3.2.2-alpine3.18
COPY --from=0 /builder /builder

RUN apk update
RUN apk add --no-cache ruby ruby-dev ruby-bundler build-base

ADD defaultBuildCmd /usr/local/bin/build

EXPOSE 8001
