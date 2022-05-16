# docker-wordpress

## Deploying Wordpress on Docker

A simple configuration to deploy a Wordpress app via docker-compose

### How to configure:

1. Modify the environment variables in the ```mysql.env``` file:

        MYSQL_ROOT_PASSWORD=<root password>
        MYSQL_DATABASE=<any db name>


2. Modify the environment variables in the ```wordpress.env``` file:

        WORDPRESS_DB_PASSWORD=<the password you entered above>
        WORDPRESS_DB_NAME=<the db name you entered above>

### How to run:

Run this script:

    docker-compose up -d

We can access the website via ```http://localhost:8080/```. The first time we access the web, it will ask us to initialize the web first.

### How to stop:

Run this script:

    docker-compose down

Running the script will not remove the data/pages we have added because it is stored in Docker volumes.