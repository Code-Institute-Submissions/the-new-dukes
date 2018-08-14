# Deployment of proyect

## This proyect was deployed through the following steps

- Creation of a server in Digital Ocean.
- Configured Nginx to serve static pages on the domain www.thenewdukes.com.
- Pulled the code down into the static serve folder from git repository https://github.com/Mgsignorelli/the-new-dukes.
- Restarted Nginx to pick up the configuration and codebase.

## The Nginx configuration used was the following:

```
server {
    listen 80 default_server;

    root /var/www/hosting/thenewdukes.com;

    index index.html index.htm;

    server_name thenewdukes.com www.thenewdukes.com;

    location / {
        try_files $uri $uri/;
    }
}
```
