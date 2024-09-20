# Cosmos Watcher Stack

This repository contains a docker compose stack for quickly deploying and managing [Cosmos Validator Watcher](https://github.com/kilnfi/cosmos-validator-watcher) instances along with supporting monitoring tools.

## Stack Components

- Cosmos Validator Watcher (multiple instances): prometheus exporter for monitoring cosmos validators.
- Prometheus: for collecting and storing metrics.
- Grafana: for visualizing metrics with dashboards.
- Loki: log aggregation.
- Promtail: log shipper for docker container logs.
