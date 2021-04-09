# free-ssl-with-certbot
how to configure apache2 with SSL and generate files


## read all about free SSL
https://letsencrypt.org/


## raspberry pi install CERTBOT
```
sudo apt install python-certbot-apache -y
sudo apt install python-certbot-nginx -y
sudo apt install certbot -y
```

## run certbot
```
sudo certbot certonly --apache
sudo certbot certonly --nginx
```

## path of generate ssl files
```
/etc/letsencrypt/live/domain.pt/privkey.pem
/etc/letsencrypt/live/domain.pt/fullchain.pem
```

## apache2 config
```
SSLCertificateFile      /etc/letsencrypt/live/domain.pt/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/domain.pt/privkey.pem
SSLCertificateChainFile /etc/letsencrypt/live/domain.pt/fullchain.pem
```
