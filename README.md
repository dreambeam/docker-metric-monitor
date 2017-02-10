# Server Metric Monitoring Framework (MMF)
## Docker-compose for the metric monitoring application


## Goal
Monitor application's metrics

## Use case
Monitor the development server environment:
- Metrics and 
- Resource usage

## Usage

## MMF Components
- Collector
StatsD daemon to collet the metrics on the server
- Aggregator
Telegraf image to aggregate the metrics: CPU, Mem, etc... and redirect them to **InfluxDB**
- InfluxDB
Time series DB, ingest the data metrics from the **Aggregator**
- Grafana
UI visualization of the metrics
