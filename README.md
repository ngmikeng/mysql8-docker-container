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
