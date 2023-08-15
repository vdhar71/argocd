#  argocd
![alt text](https://github.com/vdhar71/argocd/blob/main/argo-git.png)

This is a sample GitOps project using Java springboot petclinic application. The application is built using Gradle in a Jenkins pipeline upon any changes to the GIT repository (jenkins job gets triggered via webhook). Upon a successful build, a Docker image is created and pushed to the Docker HUB repository. The new image is then used to update the Kubernetes deployment manifests. The change in deployment manifests is detected by the 
Argo CD operator [CRD: Custom Resource Definition] running in the K8S cluster and deploys the newer image to the appropriate namespace.
