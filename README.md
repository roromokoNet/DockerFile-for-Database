# DockerFile-for-Database  
sample  

````dockerfile
FROM centos:centos7.1.1503
MAINTAINER melon
ADD MariaDB.repo /etc/yum.repos.d/MariaDB.repo
RUN yum update -y
RUN yum install -y MariaDB-server MariaDB-client
RUN yum clean all
VOLUME ["/var/lib/mysql"]
EXPOSE 3306
````
