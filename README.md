# Home Assistant Community Add-on: EMQX Enterprise

[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
[![EMQX Version][emqx-version-shield]][emqx-releases]

[![Github Actions][github-actions-shield]][github-actions]
![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

The most scalable open-source MQTT broker for IoT, IIoT, and connected vehicles. **Enterprise Edition.**

![EMQX in the Home Assistant Frontend](images/screenshot.png)

## About

[EMQX][emqx] is an Open-source MQTT broker with a high-performance real-time
message processing engine, powering event streaming for IoT devices at massive
scale. As the most scalable MQTT broker, EMQX can help you connect any device,
at any scale (including your home).

The [EMQX MQTT broker][emqx] is an advanced alternative to the Mosquitto MQTT
broker/add-on that is generally used in Home Assistant. It has a UI
to configure, manage, and debug your MQTT broker, clients, and traffic.

This fork runs the **EMQX Enterprise Edition** locally and self-hosted on your
Home Assistant instance.

[:books: Read the full add-on documentation][docs]

## Why Enterprise Edition?

The Enterprise Edition unlocks a significantly expanded feature set compared to
the open-source version:

## Key Features

EMQX delivers a powerful set of capabilities for modern connected systems:

### Comprehensive Protocol Support

- Full MQTT v5.0, v3.1.1, and v3.1 support.
- [MQTT over QUIC](https://docs.emqx.com/en/emqx/latest/mqtt-over-quic/introduction.html): Leverage the benefits of QUIC for faster connection establishment, reduced head-of-line blocking, and seamless connection migration.
- Support for other IoT protocols like [LwM2M](https://docs.emqx.com/en/emqx/latest/gateway/lwm2m.html), [CoAP](https://docs.emqx.com/en/emqx/latest/gateway/coap.html), [MQTT-SN](https://docs.emqx.com/en/emqx/latest/gateway/mqttsn.html), and more through [gateways](https://docs.emqx.com/en/emqx/latest/gateway/gateway.html).

### Massive Scalability & High Availability

- [Connect](https://www.emqx.com/en/solutions/iot-device-connectivity) 100M+ of concurrent MQTT clients with a single cluster.
- [Process](https://www.emqx.com/en/solutions/reliable-mqtt-messaging) millions of messages per second with sub-millisecond latency.
- [Masterless clustering](https://docs.emqx.com/en/emqx/latest/deploy/cluster/introduction.html) for high availability and fault tolerance.
- Seamless global communication with [EMQX Cluster Linking](https://www.emqx.com/en/solutions/cluster-linking).

### Powerful Rule Engine & Data Integration

- SQL-based [Rule Engine](https://www.emqx.com/en/solutions/mqtt-data-processing) to process, transform, enrich, and filter in-flight data.
- Seamless data bridging and [integration](https://www.emqx.com/en/solutions/mqtt-data-integration) with 50+ cloud services and enterprise systems, including:
  - **Message Queues**: [Kafka](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-kafka.html), [RabbitMQ](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-rabbitmq.html), [Pulsar](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-pulsar.html), [RocketMQ](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-rocketmq.html), etc.
  - **Databases**: [PostgreSQL](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-pgsql.html), [MySQL](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-mysql.html), [MongoDB](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-mongodb.html), [Redis](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-redis.html), [ClickHouse](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-clickhouse.html), [InfluxDB](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-influxdb.html), etc.
  - **Cloud Services**: [AWS Kinesis](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-kinesis.html), [GCP Pub/Sub](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-gcp-pubsub.html), [Azure Event](https://docs.emqx.com/en/emqx/latest/data-integration/data-bridge-azure-event-hub.html), [Confluent Cloud](https://docs.emqx.com/en/emqx/latest/data-integration/confluent-sink.html),  and more.
- [Webhook](https://docs.emqx.com/en/emqx/latest/data-integration/webhook.html) support for easy integration with custom services.

### [Message Queue](https://docs.emqx.com/en/emqx/latest/message-queue/message-queue-concept.html)

- Reliable message queuing for asynchronous and decoupled communication.
- Extends MQTT with durable message storage, configurable queue lifecycle, TTL, and size limits, ensuring messages are preserved until consumption.
- Supports load-balanced consumption and optional last-value semantics, allowing queues to retain only the most recent message for each topic when needed.

### [Flow Designer](https://docs.emqx.com/en/emqx/latest/flow-designer/introduction.html)

- Drag‑and‑drop canvas to orchestrate real‑time data pipelines with zero code, using nodes for rules, integrations, and AI tasks.

### [Smart Data Hub](https://docs.emqx.com/en/cloud/latest/data_hub/smart_data_hub.html)

- [Schema Registry](https://docs.emqx.com/en/cloud/latest/data_hub/schema_registry.html): Define, store, and manage data schemas to ensure consistency.
- [Schema Validation](https://docs.emqx.com/en/cloud/latest/data_hub/schema_validation.html): Validate incoming data against registered schemas to maintain data integrity.
- [Message Transformation](https://docs.emqx.com/en/cloud/latest/data_hub/message_transformation.html): Convert data between different formats and structures to facilitate seamless integration.

### [AI Processing & Integration](https://www.emqx.com/en/solutions/artificial-intelligence):

- Native AI processing capabilities for IoT data streams.
- Integration with popular AI services.
- Support for AI-driven decision making at the edge or in the cloud.

### Robust [Security](https://www.emqx.com/en/solutions/mqtt-security)

- [Secure connections](https://docs.emqx.com/en/emqx/latest/network/overview.html) with TLS/SSL and WSS.
- Flexible [authentication](https://docs.emqx.com/en/emqx/latest/access-control/authn/authn.html) mechanisms: username/password, JWT, PSK, X.509 certificates, etc.
- Granular access control with [ACLs](https://docs.emqx.com/en/emqx/latest/access-control/authz/authz.html).
- Integration with external authentication databases ([LDAP](https://docs.emqx.com/en/emqx/latest/access-control/authn/ldap.html), [SQL](https://docs.emqx.com/en/emqx/latest/access-control/authn/postgresql.html), [Redis](https://docs.emqx.com/en/emqx/latest/access-control/authn/redis.html)).

### Advanced Observability & Management:

- Comprehensive monitoring with [Prometheus](https://docs.emqx.com/en/emqx/latest/observability/prometheus.html), [Grafana](https://grafana.com/grafana/dashboards/17446-emqx/), [Datadog](https://docs.emqx.com/en/emqx/latest/observability/datadog.html), and [OpenTelemetry](https://docs.emqx.com/en/emqx/latest/observability/opentelemetry/opentelemetry.html).
- Detailed logging and [tracing](https://docs.emqx.com/en/emqx/latest/observability/tracer.html) capabilities.
- User-friendly [Dashboard](https://docs.emqx.com/en/emqx/latest/dashboard/introduction.html) for cluster overview and management.
- Rich [HTTP API](https://docs.emqx.com/en/emqx/latest/admin/api.html) for automation and third-party integration.

### Extensibility

- [Plugin](https://docs.emqx.com/en/emqx/latest/extensions/plugins.html) architecture for extending functionality.
- [Hooks](https://docs.emqx.com/en/emqx/latest/extensions/hooks.html) for customizing behavior at various points in the message lifecycle.



## Home Assistant MQTT Integration Setup

After starting the add-on, create a dedicated MQTT user for Home Assistant
before configuring the integration.

### 1. Create an MQTT user in EMQX

1. Open the EMQX web UI (via the **Open Web UI** button in the add-on)
2. Log in with the default credentials: `admin` / `public`
   _(change this password immediately under **System** → **Users**)_
3. Go to **Access Control** → **Authentication**
4. Select your authentication database and click **Add**
5. Create a new user — e.g. username `homeassistant`, choose a strong password

### 2. Configure Home Assistant MQTT integration

In Home Assistant, go to **Settings** → **Devices & Services** → **Add Integration** → **MQTT** and enter:

| Field | Value |
|---|---|
| Broker | `127.0.0.1` |
| Port | `1883` |
| Username | _(the user you just created)_ |
| Password | _(the password you just set)_ |

> **Note:** Use `127.0.0.1` because both Home Assistant and the EMQX add-on
> run on the same host. External devices on your network should use your Home
> Assistant's IP address instead.

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

We have set up a separate document containing our
[contribution guidelines](.github/CONTRIBUTING.md).

Thank you for being involved! :heart_eyes:

## Authors & contributors

The original setup of this repository is by [Franck Nijhof][frenck].

The Enterprise Edition fork is maintained by [Stefan Knaak][corgan2222].

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## We have got some Home Assistant add-ons for you

Want some more functionality to your Home Assistant instance?

We have created multiple add-ons for Home Assistant. For a full list, check out
our [GitHub Repository][repository].

## EMQX Enterprise License

### Important License Update

Effective from version **5.9.0**, EMQX has transitioned from Apache 2.0 to the Business Source License (BSL) 1.1.

### License Requirement for Clustering (v5.9.0+)

Starting with EMQX v5.9.0, due to the license change and the unification of all features, deploying an EMQX cluster (more than 1 node) requires a license file to be loaded.

Please refer to the following resources for details on license acquisition, application, and the specifics of the BSL 1.1.

- **News**: [EMQX Adopts Business Source License](https://www.emqx.com/en/news/emqx-adopts-business-source-license)
- **Blog**: [Adopting Business Source License to Accelerate MQTT and AI Innovation](https://www.emqx.com/en/blog/adopting-business-source-license-to-accelerate-mqtt-and-ai-innovation)
- **FAQ**: [EMQX License FAQ](https://www.emqx.com/en/content/license-faq)

## HA Addon License

MIT License

Copyright (c) 2023-2026 Franck Nijhof
Update 2026 Stefan Knaak

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[commits-shield]: https://img.shields.io/github/commit-activity/y/corgan2222/addon-emqx.svg
[commits]: https://github.com/corgan2222/addon-emqx/commits/main
[connectors]: https://docs.emqx.com/en/emqx/v5.10/data-integration/data-bridges.html
[contributors]: https://github.com/corgan2222/addon-emqx/graphs/contributors
[corgan2222]: https://github.com/corgan2222
[docs]: https://github.com/corgan2222/addon-emqx/blob/main/emqx/DOCS.md
[emqx]: https://www.emqx.io/
[emqx-releases]: https://github.com/emqx/emqx/releases/
[emqx-version-shield]: https://img.shields.io/badge/EMQX-e5.10.3-blue.svg
[flow-designer]: https://docs.emqx.com/en/emqx/v5.10/flow-designer/introduction.html
[frenck]: https://github.com/frenck
[github-actions-shield]: https://github.com/corgan2222/addon-emqx/actions/workflows/ci.yaml/badge.svg
[github-actions]: https://github.com/corgan2222/addon-emqx/actions
[issue]: https://github.com/corgan2222/addon-emqx/issues
[license-shield]: https://img.shields.io/github/license/corgan2222/addon-emqx.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2026.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[releases-shield]: https://img.shields.io/github/release/corgan2222/addon-emqx.svg
[releases]: https://github.com/corgan2222/addon-emqx/releases
[repository]: https://github.com/corgan2222/hassio-addons_repository
[rules]: https://docs.emqx.com/en/emqx/v5.10/data-integration/rules.html
[security]: https://docs.emqx.com/en/emqx/v5.10/access-control/overview.html
[webhooks]: https://docs.emqx.com/en/emqx/v5.10/data-integration/webhook.html
