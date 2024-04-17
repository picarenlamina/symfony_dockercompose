
# https://jojozhuang.github.io/architecture/creating-mysql-image-with-docker-file/
# https://es.linkedin.com/pulse/crear-una-imagen-docker-customizada-basada-en-mysql-y-morales-lemus
# https://www.baeldung.com/ops/docker-mysql-container
FROM mysql:latest
   
   
RUN chown -R mysql:root /var/lib/mysql/
   
   
ENV MYSQL_DATABASE=$MYSQL_DATABASE
ENV MYSQL_USER=$MYSQL_USER
ENV MYSQL_PASSWORD=$MYSQL_PASSWORD
ENV MYSQL_ROOT_PASSWORD=$MYSQL_ROOT_PASSWORD
  
ADD data.sql /etc/mysql/data.sql
  
RUN sed -i 's/MYSQL_DATABASE/'$MYSQL_DATABASE'/g' /etc/mysql/data.sql
RUN cp /etc/mysql/data.sql /docker-entrypoint-initdb.d
  
EXPOSE 3306
