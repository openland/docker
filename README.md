# Docker images used by Openland

## NATS

# Prepare
Generate username and password for seed node

# Run Seed node

`docker run -d --restart=always -p 4222:4222 -p 8222:8222 -p 6222:6222 --name nats-server -e NATS_USER=<user> -e NATS_PASSWORD=<password> openland/nats:v1`

# Run other nodes

`docker run -d --restart=always -p 4222:4222 -p 8222:8222 -p 6222:6222 --name nats-server -e NATS_USER=<user> -e NATS_PASSWORD=<password> openland/nats:v1 --routes=nats://<user>:<password>@<seed>:6222`