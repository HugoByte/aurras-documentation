# Docker Compose

### Prerequisites

1. [Docker](../../../../dependencies/docker/)
2. [Docker Compose](../../../../dependencies/docker-compose/)
3. [Openwhisk](../../../../dependencies/openwhisk/) \([docker-compose](../../../../dependencies/openwhisk/deployment/setup-docker-compose.md)\)

### Deployment Guide

1. Clone [aurras-deployment-docker-compose](https://github.com/HugoByte/aurras-deployment-docker-compose)

```text
git clone https://github.com/HugoByte/aurras-deployment-docker-compose
```

    2. Navigate to aurras-event-feed-substrate setup directory

```text
cd aurras-deployment-docker-compose/aurras-event-feed-substrate
```

   3. Make [configuration](../configuration.md) changes if need to local.env

   4. Run docker-compose command to start the service

```text
docker-compose --project-name aurras up -d
```

