# Define base image
FROM postgres:11.5-alpine
LABEL MAINTAINER="Chris Potter <christopher.s.potter@gmail.com>"

# Set env variables from here instead of needing to invoke via command
ENV POSTGRES_PASSWORD=Welcome

# Copying files into below folder will auto-import once DB is started in container
COPY create_database.sql /docker-entrypoint-initdb.d/1_create_database.sql
COPY create_tables.sql /docker-entrypoint-initdb.d/2_create_tables.sql
COPY insert_data.sql /docker-entrypoint-initdb.d/3_insert_data.sql
