FROM   docker.angie.software/angie:latest

ARG DOMAIN_URL
ENV DOMAIN_URL=$DOMAIN_URL

RUN apk add envsubst

CMD ["/bin/sh" , "-c" , "envsubst  '$DOMAIN_URL' < /etc/angie.conf.template > /etc/angie/angie.conf && exec angie -g 'daemon off;'"]
