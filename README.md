# Media Server Docker Compose
This repository contains the Docker Compose configuration for running my personal media server. It defines services for managing TV shows, movies, books and more using the `linuxserver.io` container images.  All services use the `/mnt/docker-volumes` directory for configuration and `/media/Lazy4Drive` for the actual media.
## Included services
Prowlarr, Sonarr, Radarr, Readarr and Whisparr for indexing media
qBittorrent and SABnzbd for downloads
Plex for streaming
Calibre and Calibre-Web for ebooks
Stash and Homarr utilities
Gluetun VPN container (used for qBittorrent and SABnzbd)

See \[`docker-compose.yml`](docker-compose.yml) for the full configuration.

## Updating containers

To update all containers to their latest images and recreate them:

```

\\\\# pull the latest images
docker compose pull

\\\\# stop existing containers and recreate
docker compose up -d --force-recreate

\\\\# (optional) clean up old images
docker image prune -a
