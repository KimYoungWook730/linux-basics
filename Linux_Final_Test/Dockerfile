FROM alpine:latest

RUN apk add --no-cache curl

COPY update.sh /usr/local/bin/update.sh
COPY cron /etc/crontabs/root

RUN chmod +x /usr/local/bin/update.sh

# VOLUME ["/data/xml"]

CMD ["crond", "-f", "-l", "8"]