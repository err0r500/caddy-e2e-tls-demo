# Caddy reverse-proxy e2e tls demo
  
## curl the backend directly : 
```
sudo docker run --rm --network ssl-demo_default -v $(pwd)/caddy/data/caddy/pki/authorities/local/root.crt:/mnt/cert.crt byrnedo/alpine-curl -v --cacert /mnt/cert.crt https:/backend.com:443
```

## curl the backend through the proxy 
```
sudo docker run --rm --network ssl-demo_default  -v $(pwd)/caddy/data/caddy/pki/authorities/local/root.crt:/mnt/cert.crt byrnedo/alpine-curl -v --cacert /mnt/cert.crt https://proxy.com:2016
```
