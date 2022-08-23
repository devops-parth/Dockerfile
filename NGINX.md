# NGINX Web Server

* HTML
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HTML 5 Boilerplate</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
        <script src="index.js"></script>
  </body>
</html>
```

* Dockerfile
```bash
FROM nginx
COPY . /usr/share/nginx/html
```

* COMMAND
```bash
docker build -t my-php-app .
docker run -it --rm --name my-running-app my-php-app
```
