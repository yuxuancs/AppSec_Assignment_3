FROM mysql:latest

COPY ./products.csv /products.csv
COPY ./users.csv /users.csv

#COPY ./setup.sql /docker-entrypoint-initdb.d/setup.sql

COPY ./migration.sql /migration.sql
COPY ./seed.sql /seed.sql

ENTRYPOINT ["/entrypoint.sh"]
CMD ["mysqld", "--secure-file-priv=/"]
