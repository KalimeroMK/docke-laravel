

### Docker requirements installation and configuration
* **Docker last version**

* **Structure add directories**
    * docker / store the Dockerfile
      * dbdata / store local db data
      * nginx / store local nginx settings
      * php / store local php settings
    * redis / store local redis dump

* **ENV**:
    * DB_HOST=mysql
    * DB_DATABASE=homestead
    * DB_USERNAME=homestead
    * DB_PASSWORD=secret

* **Domain**:
    * name.test
    * add it to host file
    * to edit domain go to .docker/nginx/conf.d/app.conf line 3

* **Docker**:
    * **In project root run**:
        * docker-compose up -d / to start all docker containers
        * docker exec -it app sh -c "php artisan migrate:fresh --seed"
        * docker-compose exec app sh / to enter application container