FROM scratch
COPY nats-server /nats-server
COPY nats-server.conf /nats-server.conf
EXPOSE 4222 8222 6222
ENTRYPOINT ["/nats-server", "--config", "nats-server.conf"]