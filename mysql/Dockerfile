
# https://jojozhuang.github.io/architecture/creating-mysql-image-with-docker-file/
# https://es.linkedin.com/pulse/crear-una-imagen-docker-customizada-basada-en-mysql-y-morales-lemus

# Base image
FROM mysql

ENV MYSQL_ROOT_PASSWORD: mypassword
ENV MYSQL_DATABASE: mydatabase

#ADD esquema.sql /docker-entrypoint-initdb.d


# Add all scripts 
COPY esquema.sql /docker-entrypoint-initdb.d/

EXPOSE 3306
