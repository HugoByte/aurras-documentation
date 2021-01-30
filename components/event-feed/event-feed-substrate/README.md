# Event Feed - Substrate

## Aurras Event Feed package to Source Events from Substrate based Chains

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

Aurras is a middleware that acts as an event processor and a low code workflow orchestration platform. This project is an Event source for Aurras system to source events from the chain.

### Configurations

Configuration values below are passed through environment variables.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Environment Variable</th>
      <th style="text-align:left">Supported Values</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">CHAIN_NAME</td>
      <td style="text-align:left"><code>CHAIN_NAME=polkadot</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li>alphanumeric string</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">CHAIN_ENDPOINT</td>
      <td style="text-align:left">
        <p><code>CHAIN_ENDPOINT=ws://localhost:9944</code>
        </p>
        <p><code>CHAIN_ENDPOINT=wss://localhost:9944</code>
        </p>
      </td>
      <td style="text-align:left">
        <p>Protocols Supported :</p>
        <ul>
          <li>ws (WebSocket)</li>
          <li>wss (WebSocket Secure)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LOGGERS</td>
      <td style="text-align:left"><code>LOGGERS=console,info;file,error,/home/event-feed.log</code>
      </td>
      <td style="text-align:left">
        <p>Loggers Available:</p>
        <ul>
          <li>console</li>
          <li>file</li>
        </ul>
        <p>Logger Levels:</p>
        <ul>
          <li>info</li>
          <li>warning</li>
          <li>error</li>
          <li>debug</li>
        </ul>
        <p>
          <br />Format:
          <br />LOGGERS=type,level[,param]
          <br />
          <br />Multiple loggers can be provided separated by &quot;;&quot;</p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">EXCLUDES</td>
      <td style="text-align:left"><code>EXCLUDES=&quot;system;balance=transfer;&quot;</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li>A Section can be excluded as whole</li>
          <li>Specific methods of the section can be excluded</li>
        </ul>
        <p>Format: EXCLUDES=&quot;section[=methods]&quot;</p>
        <p>Multiple sections to be provided separated by &quot;;&quot;</p>
        <p>Multiple methods to be separated by &quot;,&quot;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TYPES_FILE</td>
      <td style="text-align:left"><code>TYPES_FILE=&quot;/opt/types.json&quot;</code>
      </td>
      <td style="text-align:left">Location to custom types for the chain</td>
    </tr>
    <tr>
      <td style="text-align:left">KAFKA_BROKERS</td>
      <td style="text-align:left"><code>KAFKA_BROKERS=localhost:9091;localhost:9092</code>
      </td>
      <td style="text-align:left">List of Kafka brokers where the event should be posted separated by &quot;;&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">KAFKA_TOPIC</td>
      <td style="text-align:left"><code>KAFKA_TOPIC=substrate</code>
      </td>
      <td style="text-align:left">Kafka topic to which events to be posted &quot;;&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">OPENWHISK_API_KEY</td>
      <td style="text-align:left"><code>OPENWHISK_API_KEY=cafebabe-cafe-babe-cafe-babecafebabe:007zO3xZCLrMN6v2BKK1dXYFpXlPkccOFqm12CdAsMgRU4VrNZ9lyGVCGuMDGIwP</code>
      </td>
      <td style="text-align:left">Openwhisk authentication key</td>
    </tr>
    <tr>
      <td style="text-align:left">OPENWHISK_API_HOST</td>
      <td style="text-align:left"><code>OPENWHISK_API_HOST=http://localhost:3232</code>
      </td>
      <td style="text-align:left">Openwhisk API Endpoint</td>
    </tr>
    <tr>
      <td style="text-align:left">OPENWHISK_NAMESPACE</td>
      <td style="text-align:left"><code>OPENWHISK_NAMESPACE=aurras</code>
      </td>
      <td style="text-align:left">Organization space where the rules and triggers related to aurras resides</td>
    </tr>
  </tbody>
</table>

### License

Licensed under [Apache-2.0](https://github.com/HugoByte/aurras-documentation/tree/f07f6727f0cb01cccf04f15ec446e2d310ca1cb9/components/event-feed/substrate-event-feed/LICENSE/README.md)

