FROM mysql:8.0.33
ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"
ADD db-backup.sql docker-entrypoint-initdb.d/db-backup.sql
