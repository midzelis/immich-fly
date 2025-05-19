ARG CADDY_VERSION=2.10.0
FROM caddy:${CADDY_VERSION}-builder AS builder

RUN xcaddy build \
    --with github.com/mholt/caddy-events-exec \
    --with github.com/caddy-dns/cloudflare

#--with github.com/BadAimWeeb/caddy-uwsgi-transport \

FROM caddy:${CADDY_VERSION}-alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

RUN apk update && apk add nss-tools 