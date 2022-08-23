# PHP as Web Server

## Example 1
*File Available: index.php*

* Dockerfile
```sh
FROM php:7.2-apache
COPY . /var/www/html/
```
* Commands
```sh
- docker build -t my-citrio-app .
- docker run -p 8080:80 my-citrio-app
# -d flag can be used but then we have to use docker log CONTAINERID
- 
```
## Example 2
*(Not as Web Server, it will display only on CLI)*

* index.php
```php
<?php
echo "Hello World";
?>
```

* Dockerfile
```sh
FROM php:7.2-cli
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
CMD [ "php", "./index.php" ]
```
* Commands
```sh
- docker build -t my-php-app .
- docker run --rm --name hello-world-test my-php-app
```
