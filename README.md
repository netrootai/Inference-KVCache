# Netrootai Telemetry & Analysis Dashboard

> **Quick Link:** [Download the Detailed Guide PDF](Netrootai%20KV_Detailed%20Guide%20For%20github%20(2).pdf)

## Overview
The Netrootai Telemetry & Analysis Dashboard provides a consolidated view of model performance, GPU-related telemetry, KV-cache behavior, throughput, latency, and estimated infrastructure cost. It brings key indicators and time-series views into one workspace so users can review performance patterns and compare selected model and GPU configurations.

![Dashboard Overview](assets/dashboard_overview.png)

---

## 1. Key Capabilities
* **Multi-Source Data Integration:** Connect and unify telemetry from multiple Netrootai Analytics-compatible data sources, including SQL databases and time-series engines.
* **Flexible Infrastructure Scope:** Adaptable across compute workloads, covering CPU and GPU performance, memory pressure, and cluster network telemetry.
* **Interactive Dashboarding:** Enable rich visual exploration through adjustable time ranges, dynamic refresh intervals, entity-based filtering, and metric comparisons.
* **Statistical KPI Engine:** Support rolling statistical analysis, including mean, median, and standard deviation, using configurable sample windows.

---

## 2. Time-Series Visualizations & Multi-Machine Monitoring
Time-series panels render telemetry readings against unified UTC timestamps to reveal utilization spikes and cyclical profiles. Monitored nodes represent individual servers for side-by-side performance benchmarking.

![KV-Cache Utilization](assets/kv_cache_utilization.png)

---

## 3. Multiple Data-Source Integration
Netrootai supports simultaneous connections to heterogeneous backend data stores (PostgreSQL, MySQL, Prometheus, time-series engines) within a unified workspace.

![Data Sources Connection](assets/data_sources_connection.png)
![Data Source 2](assets/Data%20Source%202.png)

---

## 4. Creating Custom KPIs in Netrootai Analytics
Authorized users can author custom KPIs using native database queries directly within the panel query editor to support specialized operational needs.

![New Dashboard Editor](assets/new_dashboard_editor..png)

---

## 5. Statistical Performance Indicators
Pre-built statistical indicators calculated over a calibrated rolling window:
* **Rolling Mean:** Arithmetic average across readings to identify sustained capacity trends.
* **Rolling Median:** 50th percentile (central value) to filter transient telemetry noise.
* **Rolling Std Dev:** Dispersion relative to mean to assess workload stability and volatility.

---

## 6. Understanding the Panels

### KPI Cards
KPI cards provide a quick summary of individual metrics. Check the displayed unit before comparing values.
![KPI Card](assets/KPI_CARD.png)

### Time-Series Panels
Time-series panels show how a metric changes across the selected time range.
![Time-Series Panels](assets/ime-series%20panels.png)

### Comparison Charts
Comparison charts help identify differences between models, GPU configurations, batch sizes, or other dimensions.
![Comparison Charts](assets/Comparison%20charts%20.png)

### Model and GPU Comparison Table
The comparison table presents available metrics by model and GPU configuration.
![Model and GPU Comparison Table](assets/Model%20and%20GPU%20comparison%20table%20.png)

---

## 7. Netrootai Intelligent LLM Assistant
The Netrootai LLM Assistant transforms complex telemetry dashboards into understandable, actionable insights, providing root-cause analysis and operational recommendations.

![Business Values](assets/Buisness%20Values.png)

---

## 8. Support & Good Practices
* Keep model and GPU selections explicit when capturing screenshots or sharing findings.
* Record the selected time range when reporting a result.
* Compare metrics only when their units and definitions are aligned.
