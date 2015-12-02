# proxy-pass-with-nginx

Sample conf file

```
server {
        listen 80;
        server_name api.netplanning.thenino.net;
        location / {
                proxy_pass http://127.0.0.1:50000;
        }
}

server {
        listen 80;
        server_name netplanning.thenino.net;
        location / {
                proxy_pass http://127.0.0.1:50001;
        }
}
```
