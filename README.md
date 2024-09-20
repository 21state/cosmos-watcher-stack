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
