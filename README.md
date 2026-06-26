# solace-otel-metrics-pipeline

Companion repository for the blog post:
**[Your Solace Prometheus Exporter Deserves a Better Pipeline](hhttps://dev.to/pascalre/your-solace-prometheus-exporter-deserves-a-better-pipeline-3i6i)**

## What's in here

A minimal but production-relevant setup that routes Solace metrics through an OpenTelemetry Collector to multiple backends simultaneously.

## Getting Started

```bash
git clone https://github.com/pascalre/solace-otel-metrics-pipeline
cd solace-otel-metrics-pipeline
docker compose up
```

Prometheus: `localhost:9090`
VictoriaMetrics: `localhost:8428/vmui`

Query `solace_up` in either to verify both backends are receiving data from a single scrape.

## Requirements

- Docker + Docker Compose
- ~4GB RAM (Solace broker)
