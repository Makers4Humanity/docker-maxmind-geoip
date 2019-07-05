## maxmind-geoip Dockerfile


This repository contains **Dockerfile** of [maxmind-geoip](http://dev.maxmind.com/geoip/geoipupdate/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/alexm4h/docker-maxmind-geoip/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/alexm4h/docker-maxmind-geoip/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull alexm4h/docker-maxmind-geoip`

   (alternatively, you can build an image from Dockerfile: `docker build -t="alexm4h/docker-maxmind-geoip" github.com/alexm4h/docker-maxmind-geoip`)


### Usage

    docker run -d \
    alexm4h/docker-maxmind-geoip
    

Available environment variables:


| Environment variable | Default value | Description |
| -------------------- | ------------- | ----------- |
| CRONTAB_MAILTO | root | The cron mailto |
| CRONTAB_FREQUENCY | 0 0 * * 1 | The cron frequency to run `geoipupdate` |
| EDITION_IDS | GeoLite2-City GeoLite2-Country | The list of Maxmind GeoIP's product IDs to update separated by space |

The Dockerfile provides the `/usr/share/GeoIP` volume so you can use it as a data container.
