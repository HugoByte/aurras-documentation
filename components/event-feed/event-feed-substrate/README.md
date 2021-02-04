# Event Feed - Substrate

## Event Feed package to Source Events from Substrate based Chains

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

Aurras is a middleware that acts as an event processor and a low code workflow orchestration platform. This project is an Event source for Aurras system to source events from the chain.

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

