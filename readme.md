## docker-compose adguardhome+nginx+v2ray+ws+cloudflare+tls
### config v2ray
```
edit v2ray\config.json > uuid
```
### config nginx
```
edit nginx\conf.d\default.conf > example.com
```
### start docker
```
docker-composer up -d
```
### config cloudflare
```
dns: type: A
domain:ip

ssl-tls: Flexible

network: WebSockets:On
```
### init adguardhome
```
http://youIpHere:3000/
```
### config adguardhome
```
http://youIpHere:8080/
```

### v2ray client
```
{
  "host": "example.com",
  "port": "443",
  "id": "you uuid",
  "aid": "64",
  "net": "ws",
  "type": "none",
  "path": "/path",
  "tls": "tls"
}
```