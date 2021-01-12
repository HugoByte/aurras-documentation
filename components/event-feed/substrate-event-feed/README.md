# Substrate Event Feed

## Aurras Event Feed package to Source Events from Substrate based Chains

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

Aurras is a middleware that acts as an event processor and a low code workflow orchestration platform. This project is an Event source for Aurras system to source events from chain.

### Configurations

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Environment Variable</th>
      <th style="text-align:left">Supported Values</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Chain Name</td>
      <td style="text-align:left">Name of the chain which will be registered with the event manager. Value
        should be alphanumeric</td>
      <td style="text-align:left">CHAIN_NAME</td>
      <td style="text-align:left"><code>CHAIN_NAME=polkadot</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Chain Endpoint</td>
      <td style="text-align:left">Endpoint of the chain node to be connected. The protocol of the endpoint
        should either ws (WebSocket) or wss (WebSocket Secure)</td>
      <td style="text-align:left">CHAIN_ENDPOINT</td>
      <td style="text-align:left">
        <p><code>CHAIN_ENDPOINT=ws://localhost:9944</code>
        </p>
        <p><code>CHAIN_ENDPOINT=wss://localhost:9944</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Loggers</td>
      <td style="text-align:left">
        <p>Logging mechanism. At present only console and file loggers are supported.
          Multiple loggers can be provided seperated by &apos;;&apos; In the format
          specified:</p>
        <p>LOGGERS=type,level[,param]</p>
      </td>
      <td style="text-align:left">LOGGERS</td>
      <td style="text-align:left"><code>LOGGERS=console,info;file,error,/home/event-feed.log</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### License

Licensed under [Apache-2.0](https://github.com/HugoByte/aurras-documentation/tree/f07f6727f0cb01cccf04f15ec446e2d310ca1cb9/components/event-feed/substrate-event-feed/LICENSE/README.md)

