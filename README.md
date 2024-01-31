# Adminer eok8177 dark theme

![image](https://github.com/eok8177/adminer.css/assets/8864590/efef2242-2ee5-45b8-a6b7-f63ad7f25d38)

This is `adminer.css` file for the [Adminer](https://www.adminer.org) database manager.

For local development, it should be placed next to the `adminer.php` file

### If you run the app via Laravel Sail (Docker)

You can put the `adminer.css` file in the `public/css/adminer.php` folder. Then the config in `docker-compose.yml` will look like this:

```yml
adminer:
    image: adminer
    ports:
        - 8080:8080
    environment:
        ADMINER_DEFAULT_SERVER: mysql
    depends_on:
        - mysql
    volumes:
        - ./public/css/adminer.css:/var/www/html/adminer.css
    networks:
        - sail
```


