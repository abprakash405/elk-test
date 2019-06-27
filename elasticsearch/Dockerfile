FROM  ubuntu:latest


RUN apt-get update

RUN apt-get install apache2 -y

RUN apt-get install wget gnupg default-jdk  -y

RUN wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | apt-key add -
RUN apt-get install apt-transport-https
RUN echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | tee -a /etc/apt/sources.list.d/elastic-7.x.list
RUN apt-get update
RUN apt-get install elasticsearch curl -y
EXPOSE 80
EXPOSE 9200
EXPOSE 9300


CMD /usr/sbin/apachectl -D FOREGROUND
