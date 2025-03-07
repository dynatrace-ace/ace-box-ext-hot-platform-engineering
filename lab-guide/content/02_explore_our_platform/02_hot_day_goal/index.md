## HOT Day Goal

### Goal of this HOT Day Session

![Goal of HOT Day](../../../assets/images/02_02_goal_of_HOT_day.png)

### How we built the IDP

![How we built the IDP](../../../assets/images/02_01_built_the_idp.png)

Our platform follows the GitOps model where EVERYTHING - Platform and Services - are deployed through ArgoCD.

Our Platform and its components (backstage, dynatrace, opentelemetry, keptn, ...) is defined in Git and will be deployed by ArgoCD.

When onboarding a new application a new Git repository is created based on a template which is then also deployed by ArgoCD.

Everything that is deployed on that target K8s cluster is fully observed with Dynatrace.