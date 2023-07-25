FROM debian:bookworm-slim

RUN apt-get update \
    && apt-get install -y dnsmasq \
    && rm -rf /var/lib/apt/lists/*
    
RUN useradd -s /bin/bash masq
USER masq

EXPOSE 53

ENTRYPOINT ["dnsmasq","--no-daemon"]