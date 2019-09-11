# laravel-setup

Setup PHP-FPM + Nginx development environment.


# Start
1. copy this project
2. run `docker-compose up --build`
3. print container name
    ```
    $ docker ps -f "name=_webapp"
    CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
    48b050d3c6d7        xxxx_webapp         "docker-php-entrypoi…"   10 minutes ago      Up 10 minutes       9000/tcp            xxxx_webapp_1
    ```

4. run `docker exec -it [container name] composer create-project laravel/laravel . --prefer-dist`
5. run `chmod -R a+w webapp/storage webapp/bootstrap/cache`
6. access to `http://localhost:18001/`
