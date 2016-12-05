# Docker PHP Adapt

This is a simple Docker file to let user to change UID and GID of www-data. 

It could be used with a new Dockerfile that have only this line:

```dockerfile
FROM metal3d/php-adapt:7
```

Then, build it like this:

```
docker build -t an-image-name --build-arg WWW_GID=$(id -u) --build-arg WWW_GID=$(id -g) .
```

And now, your "an-image-name" has www-data user having the same id/gid than your working user.
