# Deployment Notes

## Environment
- Ubuntu 24.04 VPS
- Nginx + PHP-FPM + MariaDB (LEMP)
- WordPress

## Domain and DNS
- Subdomain: coach.konstadinos-tsakalakis.com
- DNS A record points the subdomain to the VPS

## Web server
- Nginx server block configured in:
  - nginx/coach.conf
- HTTPS via Let's Encrypt (Certbot)

## PHP
- WordPress served through PHP-FPM (FastCGI)

## Database
- Dedicated database and user created in MariaDB
- Credentials stored in wp-config.php (not committed)

## Validation
- nginx -t
- systemctl reload nginx
- curl checks for mixed content and correct URLs
