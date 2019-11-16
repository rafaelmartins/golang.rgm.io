# golang.rgm.io
My golang namespace.

### Example nginx configuration block

```
server {
    ...

    location / {
        try_files $uri $uri/ @redir;
    }

    location @redir {
        rewrite ^/([a-zA-Z0-9_-]+)/.+$ /$1/;
    }
}
```
