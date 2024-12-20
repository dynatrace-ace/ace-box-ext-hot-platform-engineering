## Additional Hands-On Exercises

We have some additional things for you to do in case you have time

### Explore our GitLab & Argo Dashboards

![GitLab Argo Dashboards](../../../assets/images/06_01_gitlab_argo_dashboards.png)

Explore the additional dashboards we have uploaded to the Dynatrace tenant. Gives you additional insights into ArgoCD as well as GitLab.

### Platform and application logs

![Dynatrace Logs](../../../assets/images/06_01_dynatrace_logs.png)

Explore all logs that are ingested into Dynatrace using the Logs App. Try to find any errors or patterns!

### Dynatrace Synthetic Tests

![Dynatrace Synthetics](../../../assets/images/06_01_dynatrace_synthetics.png)

Every deployed app as well as all platform components (backstage, gitlab, argo) are automatically monitored with a Dynatrace Synthetic Test. The configuration is pushed out through Monaco

Open the Dynatrace Synthetic app and explore how stable those apps are.

To learn more about Synthetics read [HTTP Monitors](https://www.dynatrace.com/news/blog/simplify-test-management-with-dynatrace-http-monitors/)

### ArgoCD Health with OpenTelemetry and Prometheus

![ArgoCD Health](../../../assets/images/06_01_dynatrace_otel_prometheus.png)

ArgoCD is exposing OpenTelemetry as well as Prometheus data
Find the ArgoCD Service and explore the traces. Also use the global metrics search and find some of the prometheus metrics!