# Conoha VPS

## DNS

|タイプ|名称|TTL|値|
|---|---|---|---|
|A(通常)|@|3600|IP Address|
|CNAME|www|3600|kazu.life|
|NS|@|3600|ns-a1.conoha.io|
|NS|@|3600|ns-a2.conoha.io|
|NS|@|3600|ns-a3.conoha.io|

## Nginx

### Usage

```bash
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
```

### Setup

```bash
mkdir /etc/nginx/sites-enabled/

ln -s /root/vps_setting/middleware/nginx/nginx.conf      /etc/nginx/nginx.conf
ln -s /root/vps_setting/middleware/nginx/nginxconfig.io  /etc/nginx/nginxconfig.io
ln -s /root/vps_setting/middleware/nginx/sites-available /etc/nginx/sites-available

ln -s /etc/nginx/sites-available/kazu.life.conf /etc/nginx/sites-enabled/kazu.life.conf
```
