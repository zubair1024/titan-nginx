# NGINX with Certbot for Let's Encrypt SSL

1. make adjustments nginx configuration to the file `conf/app.conf`.
2. add the hostnames to the `.env` file. See `example.env` for reference.
3. start the nginx instance
   ```
   docker-compose up -d
   ```
4. start certbot procedure with the appropriate hostname
   ```
   docker-compose -f ./docker-compose-certbot.yml run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ -d example.org
   ```
