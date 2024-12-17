FROM ubuntu:14.04

RUN apt-get update

RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
  wget \
  openssh-client \
  bind9 \
  bind9utils \
  bind9-doc \
  dnsutils \
  libidn11 \
  libpcre3 \
  libgmp10 \
  libexpat1 \
  libstdc++6 \
  libaio1 \
  netcat-openbsd \
  libperl5.18 \
  pax \
  sqlite3 \
  sudo \
  sysstat \
  unzip

RUN mkdir /opt/zimbra-install

COPY assets/etc /etc/
COPY assets/start.sh /opt/zimbra-install/
COPY assets/zimbra-zcs-8.6.0.tar.gz /opt/zimbra-install/
COPY assets/installZimbra-keystrokes /opt/zimbra-install/

# CMD ["/bin/bash", "/opt/zimbra-install/start.sh", "-d"]
CMD ["/bin/bash"]

# docker build -t zimbra .
# docker run -it -p 25:25 -p 80:80 -p 456:456 -p 587:587 -p 110:110 -p 143:143 -p 993:993 -p 995:995 -p 443:443 -p 8080:8080 -p 8443:8443 -p 7071:7071 -p 9071:9071 -h zimbra86-docker.zimbra.io --dns 127.0.0.1 --dns 8.8.8.8 -i -t -e PASSWORD=Zimbra2015 -e MailSSLPort=443 -e AdminPort=7071 -e AdminURL=/zimbraAdmin zimbra