FROM alpine:3.20.2
LABEL org.opencontainers.image.authors="kiarash.s@hotmail.com"
ENV REFRESHED_AT=2024-08-30
RUN adduser -H -S -s /bin/false www-data
RUN apk update; apk add --no-cache ruby ruby-dev build-base redis
RUN gem install --no-document sinatra json redis
RUN mkdir -p /opt/webapp
EXPOSE 4567
CMD [ "/opt/webapp/bin/webapp" ]
