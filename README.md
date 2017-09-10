# Wordpress with plugins deployment recipe

A basic `docker-compose.yml` for running the [wordpress-with-plugins](https://github.com/ellakcy/wordpress-with-plugins) docker solution. Perfect for running a production - ready wordpress.

## How to run:

### First run

First of all __modify__ the `.env` file accorditly (in case you do not see it then the `ls -lah` will show it). The commends will quide you what to put on each variable. Then follow one of the following command sets:

1 For apache-based wordpress:

  ```bash
  ln -s docker-compose-apache.yml ./docker-compose.yml
  docker-compose up -d
  ```

2 For fpm based wordpress

  ```bash
  ln -s docker-compose-fpm.yml ./docker-compose.yml
  docker-compose up -d
  ```

## Running new versions

In case there are new versions of the images then run the following commands (as one):

```bash
docker-compose stop && docker-compose rm && docker-compose up -d
```

## Switch between apache-based and fpm-based version

Remove the `docker-compose.yml`

```bash
rm -rf docker-compose.yml
```

Then use the commands mentioned above
