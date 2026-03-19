FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD=admin123
ENV MYSQL_DATABASE=accounts
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=admin123
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
