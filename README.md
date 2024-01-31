# Adminer eok8177 dark theme

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
