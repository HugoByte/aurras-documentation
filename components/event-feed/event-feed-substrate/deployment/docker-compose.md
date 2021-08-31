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

   4. Generate the Event ID using `register_event_source.sh` 

   5. Update the TOPICS env configuration with the generated Event ID

   6. Add custom type if any for the chain to `config/types.json`

   7. Run docker-compose command to start the service

```text
docker-compose --project-name aurras up -d
```

