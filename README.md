# Wordpress Docker bootstrap template

This repository hosts a vanilla WordPress installation in Docker. It can be used for experimentation, or as a bootstrap for locally running a WordPress website.

## Set-up

First create the file `.env` in which you set the settings for your website. For an example environment file, see the file `.env.example`.

Then install everything using Docker:

```sh
docker compose up
```

Navigate to <http://localhost>, follow the steps, and you are set!

## Accessing the files within WordPress

After running `docker compose up`, two folders will be created inside the current working directory that are mounted to the docker container: `wordpress` and `db`. These can be inspected and modified.

## Accessing the WordPress CLI

Use 

```sh
docker exec NAME-cli wp --info
```

to access the WordPress CLI, where you replace `NAME` with the website name you set in `.env`.
(For more info, see the [tutorial I followed](https://mklasen.com/adding-and-using-wp-cli-in-a-docker-compose-setup/)).


