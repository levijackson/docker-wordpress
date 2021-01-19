# Docker Wordpress
An easy way to set up a Wordpress install to do theme or plugin development.

## Setup
1. Start the containers `docker-compose up -d`
2. Install Wordpress http://localhost:8000
3. Log into PHPMyAdmin http://localhost:8080
  - use the credentials from docker-compose.yml (`MYSQL_USER` and `MYSQL_PASSWORD`)


## Working with Wordpress
The `wp-content/` directory gets mounted to the directory this runs in. It will allow you to copy plugins or themes into it from your file system easily.

## Shutting down
`docker-compose down` will turn off the containers, but the volumes will persist. If you want to start fresh and *delete* the database, run `docker-compose down --volumes` and it will delete the volumes.