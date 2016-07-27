docker-nginx
============

A high-performance Nginx base image for Docker to serve static websites. It will serve anything in the `/var/www` directory.

To build a Docker image for your site, you'll need to create a `Dockerfile`. For example, if your site is in a directory called `src/`, you could create this `Dockerfile`:

    FROM kyma/docker-nginx
    COPY src/ /var/www
    CMD 'nginx'

Docker Hub
----------
The trusted build information can be found on the Docker Hub at https://registry.hub.docker.com/u/kyma/docker-nginx/.

```dockerfile
# Guide here:
# https://github.com/KyleAMathews/docker-nginx

# Build docker file
# docker build -t CONTAINERNAME .

# Build from this repo's image
FROM kyma/docker-nginx

# Example if you wanna swap the default server file.
COPY path/to/your/default /etc/nginx/sites-enabled/default

# Add src.
COPY src/ /var/www

CMD 'nginx'
```
