FROM prom/prometheus:v2.35.0

LABEL maintainer="Mauricio Generoso"

ARG ENVIRONMENT

COPY config/prometheus-$ENVIRONMENT.yml /etc/prometheus/prometheus.yml

COPY rules/common /etc/prometheus/rules/common