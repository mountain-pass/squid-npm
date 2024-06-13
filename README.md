# Http NPM/Yarn Registry Cache

*(Updated 2024-06-13)*

A minimal docker container, running Squid on Alpine with SSLBump, designed for caching NPM/Yarn registries.

---

## Configuration

Custom URLs and Cache strategies can be updated by modifying the runtime file `squid.conf`.

---

## Build Image

```sh
docker compose build --no-cache
```

---

## Quick Start

```sh
docker compose up
```

---

## Configure NPM proxy

```sh
npm config set proxy http://localhost:3128
npm config set https-proxy http://localhost:4128
npm config set cafile "$(pwd)/example/certs/CA.pem"
```

---

## Configure Yarn proxy

```sh
yarn config set proxy http://localhost:3128 -g
yarn config set https-proxy http://localhost:4128 -g
yarn config set cafile "$(pwd)/example/certs/CA.pem" -g
```
