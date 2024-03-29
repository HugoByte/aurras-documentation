# Kubernetes

### Prerequisites

* [Kubernetes](../../../../dependencies/kubernetes/)
* [Helm](../../../../dependencies/helm.md)
* [Openwhisk](../../../../dependencies/openwhisk/) \([Kubernetes](../../../../dependencies/openwhisk/deployment/setup-kubernetes/)\)

### Deployment Guide

1. Clone [aurras-deployment-kubernetes](https://github.com/HugoByte/aurras-deployment-kubernetes) with submodules

```text
git clone https://github.com/HugoByte/aurras-deployment-kubernetes --recurse-submodules
```

   2. Navigate to aurras-event-feed-substrate setup directory

```text
cd aurras-deployment-kubernetes/aurras-event-feed-substrate
```

   3. Get InternalIP of the cluster

```text
kubectl describe nodes | grep InternalIP
```

   4. Creating mycluster.yaml with environment variables provided below with host of the **CHAIN\_ENDPOINT** and **OPENWHISK\_API\_HOST** as InternalIP of the nodes 

{% hint style="info" %}
Assuming the IP returned from the above step 3 as "192.168.65.3"
{% endhint %}

```text
env:
  - CHAIN_NAME: Node Template
  - CHAIN_ENDPOINT: ws://192.168.65.3:9944
  - LOGGERS: console,info;file,error,/logs/event-feed.log
  - EXCLUDES: system
  - TYPES_FILE: /configs/types.json #name of the types file should be types.json
  - KAFKA_BROKERS: 192.168.65.3:9092
  - OPENWHISK_API_KEY: 23bc46b1-71f6-4ed5-8c54-816aa4f8c502:123zO3xZCLrMN6v2BKK1dXYFpXlPkccOFqm12CdAsMgRU4VrNZ9lyGVCGuMDGIwP
  - OPENWHISK_API_HOST: https://192.168.65.3:31001
  - OPENWHISK_NAMESPACE: guest
  - EVENT_RECEIVER: event-receiver
  - TOPICS=balances=<Generated>
  - EVENT_PROCESSOR=substrate-event-processor
```

5. Add custom type if any for the chain to `helm/config/types.json`

6. Deploy Openwhisk using helm

```text
helm install aurras-event-feed-substrate ./helm -n aurras -f mycluster.yaml
```

  7. Get the summary of installation using

```text
helm status aurras-event-feed-substrate -n aurras
```

