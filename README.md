# orders-api

Order creation and order status API for Buildin10.

## Run locally

```bash
npm run check
npm start
```

## HTTP endpoints

- `GET /` — service metadata
- `GET /healthz` — liveness probe
- `GET /readyz` — readiness probe

## Container

```bash
docker build -t orders-api:local .
docker run --rm -p 8080:8080 orders-api:local
curl http://localhost:8080/healthz
```

The service listens on port `8080` and runs as the unprivileged `node` user.
