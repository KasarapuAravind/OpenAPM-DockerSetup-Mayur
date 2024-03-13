# open-apm-sre-demo-backend
Open-APM Monitoring Stack with Docker Compose
This repository provides a Docker Compose setup for a monitoring stack comprising Prometheus, Tempo, OpenTelemetry Collector, Mimir, and Loki. Each component plays a crucial role in monitoring, collecting, and visualizing various metrics and logs within a distributed system.

**Folder Structure**
1. prometheus: Contains Prometheus configuration files (prometheus.yml) for defining scrape targets and intervals.
2. tempo: Holds Tempo configuration files (tempo.yaml) for configuring Tempo as a distributed tracing backend.
3. otel-collector: Includes OpenTelemetry Collector configuration files (otel-collector-config.yaml) for specifying receivers and exporters.
4. mimir: Stores Mimir configuration files (mimir.yaml) for setting up Mimir as a Prometheus Remote Write exporter.
5. loki: Contains Loki configuration files (loki-local-config.yaml) for configuring Loki as a log aggregation system.
6. Docker Compose Setup
   
**The Docker Compose file (docker-compose.yml) orchestrates the deployment of the entire monitoring stack:**
1. Prometheus: Scrapes metrics from various targets using configured jobs.
2. Tempo: Provides a distributed tracing backend for storing and querying traces.
3. OpenTelemetry Collector: Collects, processes, and exports telemetry data from various sources.
4. Mimir: Exports metrics to Prometheus via Remote Write protocol.
5. Loki: Collects and stores logs from different sources for querying and visualization.

Getting Started

1. **Clone this repository:**
git clone https://github.com/inContact/open-apm-sre-demo-backend.git

2. **Navigate to the repository directory:**
'cd open-apm-sre-demo-backend'

3. **Start the monitoring stack using Docker Compose:**
'docker-compose up -d'

4. **Access the monitoring components via their respective endpoints:**
. Prometheus: http://localhost:9090
. Tempo: http://localhost:3200
. OpenTelemetry Collector: http://localhost:8888
. Mimir: No direct access, used as an exporter for Prometheus.
. Loki: http://localhost:3100