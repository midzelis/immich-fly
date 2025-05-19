FROM ghcr.io/fatedier/frps:v0.62.1

ENTRYPOINT ["/usr/bin/frps","-c","/opt/frps.toml"]

# caddy proxy
EXPOSE 443/tcp
EXPOSE 443/udp

# server
EXPOSE 7000/udp
