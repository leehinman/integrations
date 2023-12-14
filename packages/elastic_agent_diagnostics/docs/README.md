# Elastic Agent Diagnostics

The Elastic Agent Diagnostics integration allows you ingest and analysis the logs contained in the `elastic-agent diagnostics` bundle.


## Data streams

The Elastic Agent Diagnostics integration collects one type of data streams: logs.

### Fields 

**Exported fields**

| Field | Description | Type |
|---|---|---|
| @timestamp | Event timestamp. | date |
| agent.id | Unique identifier of this agent (if one exists). Example: For Beats this would be beat.id. | keyword |
| component.id |  | keyword |
| data_stream.dataset | Data stream dataset. | constant_keyword |
| data_stream.namespace | Data stream namespace. | constant_keyword |
| data_stream.type | Data stream type. | constant_keyword |
| log.level | Original log level of the log event. If the source of the event provides a log level or textual severity, this is the one that goes in `log.level`. If your source doesn't specify one, you may put your event transport's severity here (e.g. Syslog severity). Some examples are `warn`, `err`, `i`, `informational`. | keyword |
| message | For log events the message field contains the log message, optimized for viewing in a log viewer. For structured logs without an original message field, other fields can be concatenated to form a human-readable summary of the event. If multiple messages exist, they can be combined into one message. | match_only_text |
| monitoring.metrics.libbeat.output.batches.split | Number of batches split because they were too large | long |
| monitoring.metrics.libbeat.output.events.acked | Number of events acknowledged | long |
| monitoring.metrics.libbeat.output.events.batches | Number of batches sent | long |
| monitoring.metrics.libbeat.output.events.dropped | Number of dropped events | long |
| monitoring.metrics.libbeat.output.events.failed | Number of failed events | long |
| monitoring.metrics.libbeat.output.events.toomany | Number of too many events | long |
| monitoring.metrics.libbeat.output.events.total | Total number of events | long |
| monitoring.metrics.libbeat.output.write.bytes | Number of bytes written | long |
| monitoring.metrics.libbeat.output.write.errors | Number of write errors | long |
| monitoring.metrics.libbeat.pipeline.events.active | Number of events active in pipeline | long |



## Requirements

You need Elasticsearch for storing and searching your data and Kibana for visualizing and managing it.
You can use our hosted Elasticsearch Service on Elastic Cloud, which is recommended, or self-manage the Elastic Stack on your own hardware.


## Setup

For step-by-step instructions on how to set up an integration, see the
[Getting started](https://www.elastic.co/guide/en/welcome-to-elastic/current/getting-started-observability.html) guide.

