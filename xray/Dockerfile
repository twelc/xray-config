FROM alpine:latest
RUN apk add --no-cache gettext tzdata ca-certificates

COPY --from=ghcr.io/xtls/xray-core:latest /usr/local/bin/xray /usr/local/bin/xray


COPY --from=ghcr.io/xtls/xray-core:latest /usr/local/share/xray /usr/local/share/xray

ENTRYPOINT ["/bin/sh", "-c", "envsubst < /etc/xray/config.template.json | xray run -config stdin:"]
