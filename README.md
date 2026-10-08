# Docker Compose Reverse Proxy Lab

A small DevOps practice project that routes requests through Nginx to two web applications. `app1/` is served by a PHP/Apache container; `app2/` is served by Nginx Alpine. The services share the `webnet` bridge network.

## Run locally

Install Docker with Compose, then run from the repository root:

```bash
docker compose up -d
```

Open `http://localhost` after the containers start. Routing rules are in `nginx/nginx.conf`. Stop the lab with `docker compose down`.

## Layout

- `docker-compose.yml` — reverse proxy, two apps, network, and health check.
- `nginx/nginx.conf` — proxy configuration.
- `app1/` and `app2/` — content served by each container.
- `.github/workflows/` — CI workflow files.

This repository is a training lab; review the configuration before exposing it to the internet.
