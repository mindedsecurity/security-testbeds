# Zimbra v8.6

Build docker

```
docker build -t zimbra .
```

Run docker

```
docker run -it -p 25:25 -p 80:80 -p 456:456 -p 587:587 -p 110:110 -p 143:143 -p 993:993 -p 995:995 -p 443:443 -p 8080:8080 -p 8443:8443 -p 7071:7071 -p 9071:9071 -h zimbra86-docker.zimbra.io --dns 127.0.0.1 --dns 8.8.8.8 -i -t -e PASSWORD=Zimbra2015 -e MailSSLPort=443 -e AdminPort=7071 -e AdminURL=/zimbraAdmin zimbra
```

Execute install script

```
cd /opt/zimbra-install
./start.sh
```
