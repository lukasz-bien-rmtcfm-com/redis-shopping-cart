# Redis shopping cart demo

This shopping cart is using Redis and RedisJson module functionalities, allowing you to save JSON as keys using methods like json_get and json_set

![alt text](https://github.com/RemoteCraftsmen/redis-shopping-cart/blob/main/preview.png?raw=true)

## Hot to run it locally?

### Prerequisites

- Node - v12.19.0
- NPM - v6.14.8
- Docker - v19.03.13 (optional)

### Local installation

Go to server folder and then:

```
# Environmental variables

Copy `.env.example` to `.env` file and fill environmental variables

REDIS_PORT: Redis port (default: 6379)
REDIS_HOST: Redis host (default: 127.0.0.1)
REDIS_PASSWORD: Redis password (default: demo)

# Run docker compose or install redis with RedisJson module manually. You can also go to https://redislabs.com/try-free/ and obtain necessary environmental variables

docker network create global
docker-compose up -d --build

# Install dependencies

npm cache clean && npm install

# Run dev server

npm run dev
```

Go to client folder and then:

```
# Environmental variables

Copy `.env.example` to `.env` file

# Install dependencies

npm cache clean && npm install

# Serve locally

npm run serve
```

## Deployment

To make deploys work, you need to create free account in https://redislabs.com/try-free/, create Redis instance with `RedisJson` module and get informations - REDIS_ENDPOINT_URI and REDIS_PASSWORD. You must pass them as environmental variables.

### Google Cloud Run

[![Run on Google
Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run/?git_repo=https://github.com/RemoteCraftsmen/redis-shopping-cart.git)

### Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

### Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2FRemoteCraftsmen%2Fredis-shopping-cart&env=REDIS_ENDPOINT_URI,REDIS_PASSWORD)
