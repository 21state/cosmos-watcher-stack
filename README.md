# Cosmos Watcher Stack

This repository contains a docker compose stack for quickly deploying and managing [Cosmos Validator Watcher](https://github.com/kilnfi/cosmos-validator-watcher) instances along with supporting monitoring tools.

## Stack Components

- Cosmos Validator Watcher (multiple instances): prometheus exporter for monitoring cosmos validators.
- Prometheus: for collecting and storing metrics.
- Grafana: for visualizing metrics with dashboards.
- Loki: log aggregation.
- Promtail: log shipper for docker container logs.

## Configuration

The stack is pre-configured for demonstration purposes.

Update the watcher containers in `compose.yml` file to specify the validators you wish to monitor.

Refer to [cosmos-validator-watcher#usage](https://github.com/kilnfi/cosmos-validator-watcher?tab=readme-ov-file#-usage) to see available options.

The common practice is deploying one watcher instance per chain with your active validator. Remember to specify running port for each instance using `--http-addr`.

## Usage

> [!IMPORTANT]
> For production use please consider using secrets management for sensitive data such as login credentials.
> 
> Additionally, secure the Prometheus endpoint by implementing authentication.

1. Start the monitoring stack.
    ```bash
    docker-compose up -d
    ```
2. Access grafana dashboard at http://localhost:3000 (default credentials: admin/grafana).
3. Import [existing dashboard](grafana/dashboards) or create a new one.

## Dashboards

[grafana/dashboards](grafana/dashboards)

Currently there is a default dashboard available provided by [@MattKetmo](https://github.com/MattKetmo) (https://github.com/kilnfi/cosmos-validator-watcher/issues/45)
