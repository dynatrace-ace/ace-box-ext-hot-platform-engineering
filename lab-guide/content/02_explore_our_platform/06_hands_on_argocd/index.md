## Hands-On: ArgoCD

### ArgoCD: Deploys everything we have in GitLab

![ArgoCD](../../../assets/images/02_06_argocd.png)

In our platform we use ArgoCD as our GitOps tool. Besides ArgoCD there are also other GitOps tools that could be used to deploy our configuration in Git to our target Kubernetes cluster. As ArgoCD is a popular tool we decided to go with this.

**Logon to ArgoCD**
To logon to ArgoCD you need username and password from the ACE Dashboard.
BE AWARE that you will be logged in as `admin` which is a power user that has full priviliges. PLEASE DO NOT DELETE anything as this may break the experience of our training!

**What do you see in the Argo UI**
The UI provides an overview of all Argo Applications. An Argo Application is linked with configuration in Git (in our case our GitLab). Argo's job is to keep the configuration in Git IN SYNC with our target K8s cluster.
Argo follows the Operator concept which means Argo is constantly validating that the state in Git is the same as in K8s. If you change your config in Git - or if something changes in K8s - Argo's job is to bring it back in Sync. 

**What you have learned:**
ArgoCD is one option for deploying configuration to K8s following the GitOps model. In our case ArgoCD will always sync Argo Applications defined in our GitLab with our target K8s cluster.