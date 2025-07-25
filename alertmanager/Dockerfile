FROM prom/alertmanager:v0.28.1

LABEL maintainer="Mauricio Generoso"

ARG ENVIRONMENT

COPY config/alertmanager-$ENVIRONMENT.yml /etc/alertmanager/alertmanager.yml
#COPY templates/* /etc/alertmanager/
