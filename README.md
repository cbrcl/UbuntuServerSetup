
### REMOVE NGINX
```
sudo apt-get purge nginx nginx-common
```

### NGINX SETUP
```
sudo nano sites-available/default
```

### PHP CONFIG
```
sudo apt-get install php-fpm
sudo nano /etc/php/7.0/fpm/php.ini
```
```
post_max_size = 128M
upload_max_filesize = 128M
```

### PHPMYADMIN INSTALL
```
sudo apt-get install phpmyadmin
sudo nano /etc/phpmyadmin/config.inc.php
```
#### Add Line to PHPMYADMIN CONFIG FILE
```
$cfg['PmaAbsoluteUri'] =  $_SERVER[HTTP_HOST].dirname($_SERVER[SCRIPT_NAME]);
```


### NGINX, PHP COMMANDS
```
# Restart Service
sudo systemctl restart nginx

# Reload Service
sudo systemctl reload nginx

# Check Nginx Config
sudo nginx -t

# Restart PHP
sudo systemctl restart php7.0-fpm

```
