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

### [Flow Designer][flow-designer]

Visual drag-and-drop editor to build data processing pipelines. Connect MQTT
topics to external systems without writing code — wire up sources,
transformations, and outputs in a browser-based canvas.

### [Rule Engine][rules]

SQL-based engine to filter, enrich, transform, and route IoT messages in
real-time. Trigger actions based on topic patterns, payload values, or device
events.

### [Data Integration — 40+ Connectors][connectors]

Push or pull data to/from external systems out of the box:

- **Databases** — MySQL, PostgreSQL, MongoDB, Redis, ClickHouse, InfluxDB,
  TimescaleDB, Microsoft SQL Server, Oracle, Cassandra and more
- **Message queues** — Apache Kafka, RabbitMQ, Apache Pulsar, RocketMQ
- **Cloud services** — Amazon Kinesis, Amazon S3, Azure Event Hubs,
  Azure Blob Storage, GCP Pub/Sub, Snowflake
- **Other** — Elasticsearch, OpenTSDB, Apache IoTDB, HStreamDB

### [Webhooks][webhooks]

Forward any MQTT message or device event to an external HTTP endpoint with
flexible payload templating. No middleware required.

### [SSO, RBAC & Audit Logs][security]

- **Single Sign-On (SSO)** — integrate with your existing identity provider
- **Role-Based Access Control (RBAC)** — fine-grained permissions per user
- **Audit Logs** — full activity trail for compliance and debugging

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

## License

MIT License

Copyright (c) 2023-2026 Franck Nijhof

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
