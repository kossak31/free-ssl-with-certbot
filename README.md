# free-ssl-with-certbot
how to configure apache2 with SSL and generate files


## read all about free SSL
https://letsencrypt.org/


## raspberry pi install CERTBOT
```
sudo apt-get install python-certbot-apache -y
sudo apt-get install certbot -y
```

## run certbot
```
sudo certbot certonly --apache
```

## path of generate ssl files
```
/etc/letsencrypt/live/cursolinux.pt/privkey.pem
/etc/letsencrypt/live/cursolinux.pt/fullchain.pem
```

## apache2 config
```
SSLCertificateFile      /etc/letsencrypt/live/cursolinux.pt/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/cursolinux.pt/privkey.pem
SSLCertificateChainFile /etc/letsencrypt/live/cursolinux.pt/fullchain.pem
```
