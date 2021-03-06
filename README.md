
# kafka-manager-docker
[![GitHub release](https://img.shields.io/github/release/hleb-albau/kafka-manager-docker.svg?style=flat-square)](https://github.com/hleb-albau/kafka-manager-docker/)
 [![Docker Stars](https://img.shields.io/docker/stars/hlebalbau/kafka-manager.svg?style=flat-square)](https://registry.hub.docker.com/v2/repositories/hlebalbau/kafka-manager/)
 [![Docker pulls](https://img.shields.io/docker/pulls/hlebalbau/kafka-manager.svg?style=flat-square)](https://registry.hub.docker.com/v2/repositories/hlebalbau/kafka-manager/)
[![Docker Automated build](https://img.shields.io/docker/automated/hlebalbau/kafka-manager.svg?maxAge=31536000&style=flat-square)](https://github.com/hlebalbau/kafka-manager/)

## How to use this image
### Using docker
```
docker run -d \
     -p 9000:9000  \
     -e ZK_HOSTS="localhost:2181" \
     hlebalbau/kafka-manager:latest \
     -Dpidfile.path=/dev/null
```     

### Using docker-compose
```
version: '3.3'
services:
  kafka_manager:
    image: hlebalbau/kafka-manager
    ports:
      - "9000:9000"
    environment:
      ZK_HOSTS: "zoo:2181"
      APPLICATION_SECRET: "random-secret"
    command: -Dpidfile.path=/dev/null
```

## Issues

If you have any problems with or questions about this image, please contact us
through a [GitHub issue](https://github.com/hleb-albau/kafka-manager-docker/issues).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small;
i am always thrilled to receive pull requests, and do our best to process them
as fast as I can.

