# python3.6 is tested

# Aliyun DNS Authenticator plugin for Certbot

A certbot dns plugin to obtain certificates using aliyun.


## Obtain Aliyun RAM AccessKey
[https://ram.console.aliyun.com/](https://ram.console.aliyun.com/)

And ensure your RAM account has `AliyunDNSFullAccess` permission.


## Install

```bash
git clone 
cd certbot-dns-aliyun
sudo python setup.py install
```

## Credentials File

```ini
certbot_dns_aliyun:dns_aliyun_access_key = 12345678
certbot_dns_aliyun:dns_aliyun_access_key_secret = 1234567890abcdef1234567890abcdef
```

```bash
chmod 600 /path/to/credentials.ini
```


## Obtain Certificates

```bash
certbot certonly -a certbot-dns-aliyun:dns-aliyun \
    --certbot-dns-aliyun:dns-aliyun-credentials /path/to/credentials.ini \
    -d example.com \
    -d "*.example.com"
```
