FROM ubuntu
MAINTAINER Fawad Halim <fawad@fawad.net>

RUN apt-get -y update
RUN apt-get -y install unzip
ADD https://dl.bintray.com/mitchellh/consul/0.3.1_linux_amd64.zip /tmp/consul.zip
RUN cd /usr/local/sbin && \
	unzip /tmp/consul.zip
CMD /usr/local/sbin/consul agent -bootstrap -server -data-dir=/tmp/consul -client=0.0.0.0
EXPOSE 8400 8500 8600/udp
