# Certified Kubernetes Administrator (CKA)

**Disclaimer**: This is not likely a comprehensive list as the exam will be a moving target with the fast pace of k8s development - please make a pull request if there something wrong or that should be added, or updated in here.

Ensure you have the right version of Kubernetes documentation selected (e.g. v1.26 for the current exam) especially for API objects and annotations.

## Exam Objectives
* [CNCF CKA](https://www.cncf.io/certification/cka/)
* [CKA Exam Curriculum](https://github.com/cncf/curriculum/blob/master/CKA_Curriculum_v1.26.pdf)
* [Candidate Handbook](https://docs.linuxfoundation.org/tc-docs/certification/lf-handbook2)
* [Exam tips](https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad)

### [Cluster Architecture, Installation & Configuration](https://v1-26.docs.kubernetes.io/docs/concepts/architecture/) 25%
* Manage role based access control (RBAC)
  * [Authorization Overview](https://v1-26.docs.kubernetes.io/docs/reference/access-authn-authz/authorization/)
  * [K8S authorization](https://thenewstack.io/a-practical-approach-to-understanding-kubernetes-authorization/)
  * [Using RBAC Authorization](https://v1-26.docs.kubernetes.io/docs/reference/access-authn-authz/rbac/)
  * [Understanding Kubernetes RBAC](https://sysdig.com/learn-cloud-native/kubernetes-security/kubernetes-rbac/)
* [Use Kubeadm to install a basic cluster](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/)
* [Manage a highly-available kubernetes cluster](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/high-availability/)
  * [Options for High Availability Topology](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/ha-topology/)
  * [Set up a High Availability etcd Cluster with kubeadm](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/setup-ha-etcd-with-kubeadm/)
  * [Configuring each kubelet in your cluster using kubeadm](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/kubelet-integration/)
  * [Dual-stack support with kubeadm](https://v1-26.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/dual-stack-support/)
* Provision underlying infrastructure to deploy a Kubernetes cluster
* [Perform a version upgrade on a kubernetes cluster using kubeadm](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-upgrade/)
* [Implement etcd back and restore](https://v1-26.docs.kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/)

### Workloads & Scheduling 15%
* Understand deployments and how to perform rolling update and rollbacks
  * [Deployments](https://v1-26.docs.kubernetes.io/docs/concepts/workloads/controllers/deployment/)
  * [Rolling updates and rollbacks](https://v1-26.docs.kubernetes.io/docs/tutorials/kubernetes-basics/update/update-intro/)
  * [Scaling Intro](https://v1-26.docs.kubernetes.io/docs/tutorials/kubernetes-basics/scale/scale-intro/)
* Use ConfigMaps and Secrets to configure applications
  * [ConfigMaps](https://v1-26.docs.kubernetes.io/docs/concepts/configuration/configmap/)
  * [Secrets](https://v1-26.docs.kubernetes.io/docs/concepts/configuration/secret/)
  * [Configuring Redis using a ConfigMap](https://v1-26.docs.kubernetes.io/docs/tutorials/configuration/configure-redis-using-configmap/)
  * [Configuration Best practices](https://v1-26.docs.kubernetes.io/docs/concepts/configuration/overview/)
* [Know how to scale applications](https://v1-26.docs.kubernetes.io/docs/tutorials/kubernetes-basics/scale/scale-intro/)
* Understand the primitives used to create robust, self-healing, application deployments
* Understand how resource limits can affect Pod Security
  * [Resource Management for pods/containers](https://v1-26.docs.kubernetes.io/docs/concepts/configuration/manage-resources-containers/)
* Awareness of manifest management and common templating tools
  * [kustomize](https://github.com/kubernetes-sigs/kustomize)
  * [helm](https://github.com/helm/helm)

### Services and Networking 20%
* Understand host networking configuration on the control node
  * [K8S Networking demystified](https://www.stackrox.io/blog/kubernetes-networking-demystified/)
* Understand connectivity between the pods
* [Understand ClusterIP, NodePort, LoadBalancer service types and endpoints](https://v1-26.docs.kubernetes.io/docs/concepts/services-networking/service/#publishing-services-service-types)
* Know how to use Ingress controllers and Ingress resources
  * [Ingress controllers](https://v1-26.docs.kubernetes.io/docs/concepts/services-networking/ingress-controllers/)
  * [Ingress resources](https://v1-26.docs.kubernetes.io/docs/concepts/services-networking/ingress/)
* Know how to configure and use CoreDNS
  * [Using CoreDNS for service discovery](https://v1-26.docs.kubernetes.io/docs/tasks/administer-cluster/coredns/)
  * [Customizing DNS Service](https://v1-26.docs.kubernetes.io/docs/tasks/administer-cluster/dns-custom-nameservers/)
* Choose an application container network interface plugin
  * [Network Plugins](https://v1-26.docs.kubernetes.io/docs/concepts/extend-kubernetes/compute-storage-net/network-plugins/)
  * [K8s Network model](https://v1-26.docs.kubernetes.io/docs/concepts/services-networking/)
  * [Comparing CNI providers](https://kubevious.io/blog/post/comparing-kubernetes-container-network-interface-cni-providers)
  * [Compare CNI providers](https://www.suse.com/c/rancher_blog/comparing-kubernetes-cni-providers-flannel-calico-canal-and-weave/)
  * [CNI Providers](https://ranchermanager.docs.rancher.com/v2.5/faq/container-network-interface-providers)

### Storage 10%
* Understand storage classes, persistent volumes
  * [Storage classes](https://v1-26.docs.kubernetes.io/docs/concepts/storage/storage-classes/)
  * [Persistent volumes](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/)
* [Understand volume mode, access modes, and reclaim policies for volumes](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes)
  * [Volume Mode](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/#volume-mode)
  * [Access Modes](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/#access-modes)
  * [Reclaim Policies](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/#reclaim-policy)
* Understand persistent volume claims primitive
  * [PVC](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/#persistentvolumeclaims)
* Know how to configure applications with persistent storage
  * [Claims as volumes](https://v1-26.docs.kubernetes.io/docs/concepts/storage/persistent-volumes/#claims-as-volumes)
  * [Configure Persistent Volume Storage](https://v1-26.docs.kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)

### Troubleshooting 30% 
* Evaluate cluster and node login
  * [Logging Architecture](https://v1-26.docs.kubernetes.io/docs/concepts/cluster-administration/logging/)
  * [K8S logging best practices](https://platform9.com/blog/kubernetes-logging-best-practices/)
* Understand how to monitor applications
  * [Debug Running Pods](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-application/debug-running-pod/)
  * [Interact with running pods](https://v1-26.docs.kubernetes.io/docs/reference/kubectl/cheatsheet/#interacting-with-running-pods)
* Manage container stdout & stderr logs
  * [kubectl commands - logs](https://v1-26.docs.kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#logs)
  * [How to find your GKE logs](https://cloud.google.com/blog/products/management-tools/finding-your-gke-logs)
  * [Enable Log Rotation in Kubernetes Cluster](https://vividcode.io/enable-log-rotation-in-kubernetes-cluster/)
* Troubleshoot application failure
  * [Debug Pods](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-application/debug-pods/)
* Troubleshoot cluster component failure
  * [Troubleshoot cluster](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-cluster/)
  * [Control plane Components](https://v1-26.docs.kubernetes.io/docs/concepts/overview/components/#control-plane-components)
  * [Node Components](https://v1-26.docs.kubernetes.io/docs/concepts/overview/components/#node-components)
  * [Debugging Kubernetes nodes with crictl](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-cluster/crictl/)
  * [Monitor Node Health](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-cluster/monitor-node-health/)
  * [Debugging Nodes with kubectl](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-cluster/kubectl-node-debug/)
  * [Looking at logs](https://v1-26.docs.kubernetes.io/docs/tasks/debug/debug-cluster/#looking-at-logs)
* Troubleshoot networking
  * [Flabbel debugging](https://github.com/flannel-io/flannel/blob/master/Documentation/troubleshooting.md#kubernetes-specific)
  * [Troubleshooting CNI plugin-related errors](https://v1-26.docs.kubernetes.io/docs/tasks/administer-cluster/migrating-from-dockershim/troubleshooting-cni-plugin-related-errors/)
  * [Debugging DNS resolution](https://v1-26.docs.kubernetes.io/docs/tasks/administer-cluster/dns-debugging-resolution/)

## Tips:
* [kubectl cheal sheet](https://v1-26.docs.kubernetes.io/docs/reference/kubectl/cheatsheet/)
* [kubectl explain](https://blog.heptio.com/kubectl-explain-heptioprotip-ee883992a243)
* [kubectl cheatsheet](https://kubernetes.io/docs/user-guide/kubectl-cheatsheet/)
* When using kubecctl for investigations and troubleshooting utilize the wide output it gives your more details
```
kubectl get pods -o wide --show-labels --all-namespaces
```
* In `kubectl` utilize `--all-namespaces` to ensure deployments, pods, objects are on the right name space, and right desired state

* for events and troubleshooting utilize kubectl describe
```
kubectl describe pods <PODID>
```
* the '-o yaml' in conjunction with `--dry-run` allows you to create a manifest template from an imperative spec, combined with `--edit` it allows you to modify the object before creation
```
kubectl create service clusterip my-svc -o yaml --dry-run > /tmp/srv.yaml
kubectl create --edit -f /tmp/srv.yaml
```

## Do you want more?
- [Kubernauts resources list](https://docs.google.com/spreadsheets/d/10NltoF_6y3mBwUzQ4bcQLQfCE1BWSgUDcJXy-Qp2JEU/edit#gid=0)
