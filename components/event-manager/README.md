# Core

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

### Introduction

Aurras is a middleware that acts as an event processor and a low code workflow orchestration platform. Aurras is being pitched as a next-generation system for enabling decentralized push notification. This middleware solution listens to events from blockchain applications and propagates them to a registered pool of MQTT brokers. The broader architecture consists of parachain from which the middleware listens for the events.

The Event Manager as a core component of the aurras system is composed of multiple actions including using a database to store trigger URLs and their respective auth, and Kafka provider, consumer, and producer. Once the event manager receives an event from the event feed, this data is produced to a topic. The feed action in the manager lets the user hook into the system. That is, once an event is indexed to a particular topic, it can invoke a particular action. While creating the workflow, users can choose the event trigger as feed and provide necessary parameters from which chain it should be listening to.

### Prerequisites

1. [Openwhisk](../../dependencies/openwhisk/)
2. [Openwhisk CLI](https://github.com/apache/openwhisk-cli)

### Components

#### Actions

* Event Register
* Event Receiver
* Event Processor
* Event Producer
* Kafka Provider
* Balance Filter
* Balance Notification Register
* Push Notification

### Installation

Assuming basic dependency such as [git](https://git-scm.com/) and [yarn](https://yarnpkg.com/) already installed.

1. Clone the repository

```text
git clone https://github.com/HugoByte/aurras.git
```

  2. Navigate to the cloned directory

```text
cd aurras
```

  3. Deploy the actions using the deploy script. The script supports optional parameters which can be found [here](configuration.md).

```text
./deploy.sh
```

### Usage

Generate Event Registration ID

```text
./register_event_source.sh --name "Node Template Balance"
```

### Testing

Run Unit test suites

To test push-notification action it is required to have a push notification token generated from the client and Firebase API Key in TEST\_DEVICE\_TOKEN and FIREBASE\_API\_KEY environment variable respectively

```text
cargo test --all-features
```

### License

Licensed under [Apache-2.0](https://github.com/HugoByte/aurras-documentation/tree/f07f6727f0cb01cccf04f15ec446e2d310ca1cb9/components/event-feed/substrate-event-feed/LICENSE/README.md)

