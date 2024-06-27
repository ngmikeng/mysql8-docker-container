# mysql8-docker-container

## Setup MySQL container for studying

```shell
# Delete unnecessary files and data in the data directory
$ rm -rf ./docker/db/data/*

# Create and start container
$ docker-compose up --build -d

# Check that the container is running
$ docker-compose ps

# Run the DB initial setting shell
$ bash ./init-mysql.sh
```

## Using container
```shell
# Start at the folder contains the file docker-compose.yml
$ docker compose start

# Start with a path pointing to the file docker-compose.yml
$ docker compose -f ~/sources/docker-composers/mysql8-docker-container/docker-compose.yml start
```

## Work with MySQL CLI
```shell
# Access to mysql container
$ docker exec -it mysql8 mysql -u dev_user -p


# mysql useful commands
show databases;
create database [database];
use [database];
show tables;

# Determine what database is in use
select database();

# Show table structure
describe [table];

# List all indexes on a table
show index from [table];
```