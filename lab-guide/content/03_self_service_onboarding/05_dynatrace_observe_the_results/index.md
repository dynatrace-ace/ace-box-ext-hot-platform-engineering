## Dynatrace: Observe the Results

### Backstage Integration: Direct Access to Dynatrace Data

![Backstage Integration](../../../assets/images/03_05_backstage_integration.png)

1. From the Backstage component page, locate the `Kubernetes Deployments` section.  This section is populated via a live query of the Dynatrace environment.  Once the Kubernetes deployment for the application is running and observed by Dynatrace, the details will appear here.

2. Under the `Workload` column, click on the workload name to open the workload in Dynatrace.  Explore the metadata, observability, security, and contextual information captured by Dynatrace automatically.

### Dynatrace Release Awareness

![Release Awareness on Workflow](../../../assets/images/03_05_dt_release_aware_workload.png)

On the `Info` section of the workload, you'll find details about the application release product, stage, and version.  Additionally, you'll find the team ownership details.  This metadata is automatically picked up from the application manifests.

![Release Awareness on Service](../../../assets/images/03_05_dt_release_aware_service.png)

On the `Overview` section of the workload, you'll find the Application Observability details.  Click on `Go to Services app` to view the Service details.  Explore the information captured by Dynatrace OneAgent through distributed tracing and code-level visibility.

![Release Awareness on Trace](../../../assets/images/03_05_dt_release_aware_trace.png)

From the top of the Service details, click on `View traces` to see the individual transactions captured as distributed traces.  Explore the waterfall details and release context information on each transaction.

### Dynatrace Monaco (Configuration as Code)

![ArgoCD Workflow for Monaco](../../../assets/images/03_05_argocd_monaco.png)

From the GitLab repo page, check the manifest `workflow-post-sync-apply-monaco.yml`.  This contains the details on how Monaco is called to apply configurations for Dynatrace owners, slos, and synthetic monitors.

### Software Delivery Lifecycle Events

![ArgoCD Notification Events](../../../assets/images/03_05_argocd_notifications_events.png)

From the GitLab `platform` repo, check the manifest `argocd-notifications-cm.yml`.  This contains the details on how ArgoCD is sending SDLC events to Dynatrace via webhooks.  These events then trigger the Lifecycle Events Workflow automation in Dynatrace, adding additional SDLC event generation and notifications to Backstage.

![Lifecycle Events Workflow](../../../assets/images/03_05_dt_lifecycle_events_workflow.png)

In the Dynatrace environment, open the Workflows app.  Locate and open the `Lifecycle Events Workflow`.  Events from ArgoCD trigger this workflow to execute.  This workflow will validate that deployments are successful when they are observed by Dynatrace.

![Platform Dashboard](../../../assets/images/03_05_dt_platform_dashboard.png)

From the Dashboards app or from the Platform Engineering Launchpad, open the `Platform Observability Cockpit` dashboard.  This dashboard queries the SDLC events and visualizes the various activites for your application's lifecycle.

### Backstage Notifications for Closed-Loop Delivery

![Backstage Notifications](../../../assets/images/03_05_backstage_notifications.png)

In Backstage, click on `Notifications` in the bottom left corner.  Select your team's channel and view the notifications sent from Dynatrace.