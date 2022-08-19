# grafana-prometheus

Grafana with prometheus docker

## Prerequisites

- Docker
- Docker-compose
- Dashy in your discord server
- git

follow [this guide](https://dash.website-v2-8pf.pages.dev/dashy) for info on how to add dashy

## Getting started

clone this repository and cd into it

```sh
git clone git@github.com:AethorBot/grafana-prometheus.git
cd grafana-prometheus
```

create a prometheus.yml file with the data you got from dashy when you ran /setup

```
nano prometheus.yml
```

example file

```yml
scrape_configs:
  - job_name: "dashy"
    scrape_interval: 30s
    metrics_path: /api/guild/867401290153590784/metrics
    bearer_token: jkadjsls
    static_configs:
      - targets: ["aethor-api.tricked.pro"]
```

run `docker-compose up -d` and the dashboard is up.

Go to localhost:3000 the username and password are admin

## Sharing dashboards with others

see [/dashboard/README.md](./dashboards/README.md)
