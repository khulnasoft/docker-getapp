FROM mariadb:10.6

LABEL maintainer="info@khulnasoft.com"

# Add GetApp schema and tables
ADD ./all.sql /docker-entrypoint-initdb.d/all.sql

RUN chown -R mysql:mysql /docker-entrypoint-initdb.d/