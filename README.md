# Platform Engineering - Use Case

## Description

Scenario that demonstrates a reference IDP (Internal Development Platform) that provides self-service onboarding of new applications on a k8s cluster with automated best-practices for Dynatrace observability.

Those best practices include
- Automatic Synthetic Tests for deployed application
- Automatic Ownership and Release Metadata on deployed workloads
- Automatic Deployment Events that allow triggering of an SRG upon a deployment change
- Automatic Service Level Objectives for new app
- Automatic push of relevant Dynatrace data back to the engineer, e.g: Backstage, Slack

Here are the tools that make up the reference IDP:
- Backstage as the IDP
- GitLab as the Git System with projects for the platform and application templates
- ArgoCD as the GitOps Operator
- Keptn to provide additional deployment insights
- ArgoRollouts for progressive rollouts
- ArgoWorkflows to trigger Monaco to push Dynatrace configuration

## Guide

This is still work in progress and will be delivered for the HOT (Hands-On Training) Day at Perform 2025

## Version and compatibility

Please add a note pointing out which versions of the external use case are compatible with the respective ACE-Box versions:

| Release | Verified against ace-box version |
| --- | --- |
| v0.9.3 | v1.27.0 |
| v0.9.5 | v1.28.0 |

## Extra variables

No extra variables needed

## DTU provisioning

When an ACE-Box with external use case is provisioned by the DTU team, make sure to grant read access to the Github [ace-box-dtu](https://github.com/orgs/dynatrace-ace/teams/ace-box-dtu) team. This allows them to source the use case during their provisioning process.


## Additional optional configuration

Here some additional OpenPipeline Configuration to correctly parse the log status from the simplenodeservice demo application.

**Pipeline**: `OTel Simplenode Ingest`
- DQL Processor: `Parse Log  Legel`
  - Matching condition: `isNotNull(content) and content != ""`
  - DQL processor definition: `parse content, "JSONTIMESTAMP ' - ' STRING:logstatus"`
- Add fields: `Add LogLevel for empty log lines`
  - Matching condition: `isNull(content) or content == "" or content == " "`` 
  - Fields: `logstatus:Empty`

**Dynamic Route**: `otel simplenode`
- Matching condition: `matchesPhrase(k8s.namespace.name,"simplenodeservice")`