# Event Feed - Substrate

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

### Introduction

Aurras is a middleware that acts as an event processor and a low code workflow orchestration platform. Aurras is being pitched as a next-generation system for enabling decentralized push notification. This middleware solution listens to events from blockchain applications and propagates them to a registered pool of MQTT brokers. The broader architecture consists of parachain from which the middleware listens for the events.

This Event Feed package facilitates to source events from substrate-based chains. The events will be posted to the OpenWhisk system. [polkadot-js/api](https://github.com/polkadot-js/api) is used under the hood to establish the connection to blockchain nodes and receive events.

### Prerequisites

1. [Substrate Based Chain](https://substrate.dev/docs/en/tutorials/create-your-first-substrate-chain/)
2. [Aurras Core](../../event-manager/)

### Installation

Assuming basic dependency such as [git](https://git-scm.com/) and [yarn](https://yarnpkg.com/) already installed.

1. Clone the repository

```text
git clone https://github.com/HugoByte/aurras-event-feed-substrate-js.git
```

  2. Navigate to the cloned directory

```text
cd aurras-event-feed-substrate-js
```

  3. Install dependencies

```text
yarn install
```

### Configuration

Configurations are passed through environment variables which can be found [here](configuration.md).

For local development and testing create a **.env** file with respective configurations in the project root folder.

```text
CHAIN_NAME=Node Template
CHAIN_ENDPOINT=ws://localhost:9944
LOGGERS=console,info;file,error,/logs/event-feed.log
EXCLUDES=system
TYPES_FILE=/configs/types.json
KAFKA_BROKERS=localhost:9092
TOPICS=balances=c76b7a5d-d18a-43e6-a28f-db6bb7520986
OPENWHISK_API_KEY=23bc46b1-71f6-4ed5-8c54-816aa4f8c502:123zO3xZCLrMN6v2BKK1dXYFpXlPkccOFqm12CdAsMgRU4VrNZ9lyGVCGuMDGIwP
OPENWHISK_API_HOST=https://localhost:31001
OPENWHISK_NAMESPACE=guest
EVENT_RECEIVER=event-receiver
EVENT_PROCESSOR=substrate-event-processor
```

### Usage

Start the feed in development mode.

```text
yarn serve
```

### Testing

Run Unit test suites

```text
yarn test
```

### Deployment

Deployment is done through either docker-compose or Kubernetes which can be found [here](deployment/).

### License

Licensed under [Apache-2.0](https://github.com/HugoByte/aurras-documentation/tree/f07f6727f0cb01cccf04f15ec446e2d310ca1cb9/components/event-feed/substrate-event-feed/LICENSE/README.md)

