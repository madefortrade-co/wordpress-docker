# Wordpress Docker Compose

This compose file will spin up a local Wordpress instance and the associated MySQL database.

## Working with the containers

Run these commands in the project directory

Deploy the containers:
```
$ docker compose up
```
Start the containrs once deployed:
```
docker compose start -d
```
Stop the containers:
```
docker compose stop
```

Stop and remove the containers:

```
$ docker compose down
```

Stop wnd remove the containers and destroy all Wordpress data
```
$ docker compose down -v
```

## Secrets

This composer file uses Docker secrets to hold sensitive information. Create a folder in the project directory called ```secrets``` and place the following files in the directory. These files must be populated in order to deploy the containers.

| File name | Contents |
| --- | --- |
| db-name | Name to be given to Wordpress database |
| db-usr | Name of user to be created in Wordpress database |
| db-pwd | Password for created user |
| db-root-pwd | Password for the root account |