# ---- Filebeat ----

ARG ELK_VERSION
FROM docker.elastic.co/beats/filebeat:${ELK_VERSION}
USER root

# ---- PostgreSQL ----

FROM postgres
CMD ["postgres", "-c", "logging_collector=on", "-c", "log_directory=/var/log/postgresql/", "-c", "log_filename=postgresql.log", "-c", "log_statement=all"]