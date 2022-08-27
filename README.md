# Observability tools
[![Prometheus](https://github.com/groot-mg/observability-tools/actions/workflows/prometheus-ci-check.yml/badge.svg)](https://github.com/groot-mg/observability-tools/actions/workflows/prometheus-ci-check.yml) [![AlertManager](https://github.com/groot-mg/observability-tools/actions/workflows/alertmanager-ci-check.yml/badge.svg)](https://github.com/groot-mg/observability-tools/actions/workflows/alertmanager-ci-check.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/groot-mg/observability-tools/blob/main/LICENSE)

This repository contains configuration for Prometheus, Alert Manager and Grafana dashboards.

## How to run

Use the local setup on the repository [docker-local-setup](https://github.com/groot-mg/docker-local-setup).

`docker-local-setup` will clone this repository and run the tools together with the services where the metrics are provided.
 
## Tools
### Prometheus

Prometheus scrapes metrics from the services/container.

The local config is on the file [prometheus-local.yml](prometheus/config/prometheus-local.yml)

### Alert Manager

Alert Manager connects to Slack Channel. Some rules are defined on Prometheus [/prometheus/rules](https://github.com/groot-mg/observability-tools/tree/main/prometheus/rules), but the Slack Channel is not automatically provided.

You need to set up the Slack Channel and change the Slack Channel url on [alertmanager/config/alertmanager-local.yml](https://github.com/groot-mg/observability-tools/blob/main/alertmanager/config/alertmanager-local.yml) and change `api_url`.

### Grafana

Dashboards are already provided inside Grafana. 

During the container startup, a backup will be loaded and all dashboards will be available, just access the local address `http://localhost:3000` and provides the default user and password `admin`. 