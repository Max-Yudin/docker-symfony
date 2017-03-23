FROM ubuntu:latest

RUN apt-get update \
&& echo "mysql-server mysql-server/root_password password 111" | debconf-set-selections \
&& echo "mysql-server mysql-server/root_password_again password 111" | debconf-set-selections \
&& apt-get install -y mysql-server

CMD ["mysqld_safe", "--bind-address=0.0.0.0"]