# Standalone Docker Image

OpenWhisk standalone server is meant to run a simple OpenWhisk server for local development and test purposes. Standalone controller image published as `openwhisk/standalone:nightly` is used for development.

The below configuration is provided in the docker-compose configuration

{% tabs %}
{% tab title="Openwhisk Standalone Docker Compose Configuration" %}
{% code title="docker-compose.yaml" %}
```yaml
openwhisk-standalone:
    image: openwhisk/standalone:nightly
    container_name: openwhisk
    hostname: openwhisk
    environment:
      - JVM_EXTRA_ARGS=-Dwhisk.users.aurras-system=cafebabe-cafe-babe-cafe-babecafebabe:007zO3xZCLrMN6v2BKK1dXYFpXlPkccOFqm12CdAsMgRU4VrNZ9lyGVCGuMDGIwP -Dwhisk.container-factory.container-args.network=aurras
    networks:
      - aurras
    ports:
      - "3233:3233"
      - "3232:3232"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    command: --enable-bootstrap
```
{% endcode %}
{% endtab %}
{% endtabs %}



