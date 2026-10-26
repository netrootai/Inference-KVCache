# Inference-KVCatch

Netroot AI --- Telemetry & Analysis Dashboard

Overview

The Netroot AI Telemetry & Analysis Dashboard provides a consolidated
view of model performance, GPU-related telemetry, KV-cache behaviour,
throughput, latency, and estimated infrastructure cost. It brings key
indicators and time-series views into one workspace so users can review
performance patterns and compare selected model and GPU configurations.

What you can monitor

Depending on the panels enabled in your deployment, the dashboard can
include:

Mean KV-cache memory utilization (%) --- overview of cache
capacity usage.

Cache eviction rate (%) --- rate of cache eviction events.

Time to First Token (TTFT) --- time before the first output
token is produced.

Time per Output Token (TPOT) --- time associated with producing
subsequent output tokens.

Throughput (tokens/sec) --- token generation throughput.

KV-cache compression ratio --- compression achieved for cache
data.

Latency overhead (%) --- additional latency associated with the
measured configuration.

Estimated GPU cost per minute ($) --- estimated cost indicator
for the selected configuration.

KV-cache memory by model --- comparison of memory consumption
across models.

Dynamic memory pressure heatmap --- visual overview of
memory-pressure patterns across displayed time points and series.

KV-cache memory utilization over time --- time-series view of
utilization changes.

Throughput by batch size --- comparison of throughput across
batch sizes.

KV-cache memory vs. throughput --- view of the relationship
between memory consumption and throughput.

Model and GPU comparison table --- tabular view of metrics for
selected model/GPU combinations.

Metric availability depends on the panels and fields configured in the
deployed dashboard.

Opening the dashboard

Open the Netroot AI Telemetry & Analysis Dashboard using the URL
supplied by your administrator or project team.

Sign in if your deployment requires authentication.

Open the relevant telemetry dashboard from the dashboard navigation.

Use the time-range control to select the period you want to inspect.

Use the dashboard refresh control to refresh the displayed panels.

The dashboard URL, access method, and authentication requirements depend
on the deployment environment.

Using the model and GPU filters

The dashboard provides model and GPU selectors at the top.

Select a model

Open the Select AI Model filter.

Choose one or more available model names.

Apply the selection if the interface requires confirmation.

Review the KPI cards, charts, and table for the selected models.

Select a GPU

Open the Select GPU filter.

Choose one or more available GPU types.

Apply the selection if required.

Review the updated dashboard panels.

Compare configurations

Select the models you want to inspect.

Select the GPU types you want to compare.

Review the KPI cards for a quick summary.

Use the model-level charts and comparison table to inspect the
available breakdown.

Change one filter at a time when investigating differences between
configurations.

The available combinations depend on the records and configuration
exposed by the connected telemetry data source.

Understanding the panels

KPI cards

KPI cards provide a quick summary of individual metrics. Check the
displayed unit before comparing values. For example, KV-cache memory in
GB and KV-cache utilization in percent measure different things and
should not be expected to have the same numeric value.

Time-series panels

Time-series panels show how a metric changes across the selected time
range. Use the time-range selector and refresh controls to review the
period of interest. The displayed time range and refresh interval are
controlled by dashboard settings.

Comparison charts

Comparison charts help identify differences between models, GPU
configurations, batch sizes, or other dimensions exposed by a panel.
Check axis labels and units before drawing conclusions.

Model and GPU comparison table

The comparison table presents available metrics by model and GPU
configuration.

Set the model and GPU filters first.

Confirm that the table contains the configurations you intended to
review.

Read each value alongside its column heading and unit.

Use the timestamp or time-range context where available.

When comparing a table value with a KPI, verify that both panels use
the same metric definition, filters, time range, and aggregation
method. Values can differ when panels use different sources or
calculations.

Refreshing and time ranges

Use the time-range selector to choose the period to inspect.

Use the refresh control to request an updated view.

An automatic refresh interval, when enabled, determines how often
panels are queried again.

A refresh requests the latest information available through the
configured data source; it does not by itself guarantee that new
telemetry records have been ingested.

If the dashboard appears unchanged, verify the selected time range,
refresh interval, data-source connection, and availability of recent
records.

Local access and environment setup

The exact local startup command depends on the repository and deployment
configuration used by your team. Use the project's existing environment
configuration and startup instructions rather than creating a separate
instance with different settings.

Before running the dashboard locally, confirm:

The required runtime and dependencies are installed.

The dashboard service is configured for the intended local address
and port.

The telemetry database is reachable from the local environment.

The configured data-source connection uses the correct host, port,
database, and credentials.

Required network access and database permissions are in place.

Secrets and passwords are supplied through the approved environment
or secret-management mechanism, not committed to source control.

After startup, open the configured local address in a browser and follow
the Opening the dashboard and Using the model and GPU filters
sections above.

Configuration note: Hostnames, ports, credentials, and startup
commands vary by deployment. Use the values maintained by your project
team.

Troubleshooting

The dashboard does not load

Confirm that the dashboard service is running.

Verify the URL, port, network access, and authentication
requirements.

Review service logs for startup or configuration errors.

A panel reports a query or data-source error

Confirm that the configured data source is available.

Check the database name, table names, column names, and permissions.

Review the panel query for syntax errors and confirm that referenced
dashboard variables exist.

A model or GPU selection returns no rows

Confirm that the selected model and GPU names are available in the
connected data source.

Try selecting one model and one GPU at a time.

Check whether the selected combination has records in the chosen
time range.

KPI values do not match the comparison table

Values match only when the KPI and table use the same metric definition,
source, filters, time range, and calculation. Check whether one panel
uses a stored database field while another uses a separate calculation,
and whether the panels use different rounding or aggregation rules.
Align those definitions before treating the values as directly
comparable.

Values do not appear to update

Trigger a manual refresh.

Check the dashboard's automatic refresh interval.

Confirm that the selected time range includes the relevant records.

Verify that the upstream telemetry process is delivering updated
records to the configured data source.

A metric has an unexpected unit or sign

Check the panel title, axis label, and unit configuration.

Verify the field mapping and calculation used by the panel.

Confirm that the metric definition and expected range are documented
for the deployment.

Good practices

Keep model and GPU selections explicit when capturing screenshots or
sharing findings.

Record the selected time range when reporting a result.

Compare metrics only when their units and definitions are aligned.

Use the table for configuration-level inspection and charts for
patterns over time.

Avoid interpreting a displayed value without checking its unit and
panel definition.

Report persistent errors with the panel name, selected filters, time
range, and relevant error message. Never include passwords, tokens,
or other secrets in a report.

Support

For access issues, environment setup, missing configurations, or
unexpected telemetry results, contact the Netroot AI project or platform
administrator. Include the dashboard panel name, selected model/GPU
filters, time range, and relevant error details.



