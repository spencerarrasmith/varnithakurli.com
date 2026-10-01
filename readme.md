# Readme

## Local development
While the website contents are built into the container, the local development directory may be mounted into the container directly for more rapid iteration:

`docker build -t varnithakurli.com:dev .`

`docker run -d --name varnithakurli-dev --restart unless-stopped -p 127.0.0.1:8001:80 -v {project dir}/html:/usr/share/nginx/html:ro varnithakurli.com:dev`

## Releases
A Github Action will trigger a container build upon creation of a new tag at the remote:

`git tag {version}`

`git push --tags`

## Deployment
The container is available at `ghcr.io/varnithakurli/varnithakurli.com:latest` or a specific tag. This has been configured within `docker-compose.yml`:

```yml
services:

  varnithakurli:
    image: ghcr.io/varnithakurli/varnithakurli.com:latest
    container_name: varnithakurli-nginx
    restart: unless-stopped
    ports:
      - "127.0.0.1:8001:80"
```

The only commands required to pull the latest version are:

`docker compose down`

`docker compose up`