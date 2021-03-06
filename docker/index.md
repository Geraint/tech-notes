# Docker

## Attaching to a running container

```
docker exec -it <container-name> /bin/bash
```

## Installing composer

In your `Dockerfile`:

```
RUN apt-get update \
 && apt-get install curl \
 && curl -o /tmp/composer-setup.php https://getcomposer.org/installer \
 && curl -o /tmp/composer-setup.sig https://composer.github.io/installer.sig \
 && php -r "if (hash('SHA384', file_get_contents('/tmp/composer-setup.php')) !== trim(file_get_contents('/tmp/composer-setup.sig'))) { unlink('/tmp/composer-setup.php'); echo 'Invalid installer' . PHP_EOL; exit(1); }" \
 && php /tmp/composer-setup.php --no-ansi --install-dir=/usr/local/bin --filename=composer --snapshot \
 && rm -f /tmp/composer-setup.*
```

## Ignoring composer's pesky symbolic links

In `<project-root>/.dockerignore`

```
/vendor/bin/*
```

## Deleting Artifacts

```
docker system prune --all --force
```

## External Links

- [Useful Docker Commands and Aliases](https://medium.com/devopslinks/useful-docker-commands-and-aliases-9ea79191832f)

