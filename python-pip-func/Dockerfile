From alpine:3.3

# add our user and group first to make sure their IDs get assigned consistently, regardless of whatever dependencies get added
RUN addgroup -S vijay && adduser -S -G vijay vijay

# grab su-exec for easy step-down from root
RUN apk add --no-cache 'su-exec>=0.2'

RUN mkdir -p /apps/python-app && chown vijay:vijay /apps/python-app

ADD . /apps/python-app
WORKDIR /apps/python-app

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]
