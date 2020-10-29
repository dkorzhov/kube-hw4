It checked on minikube.

HW 4-1
Pods kube-system:

1. coredns-66bff467f8-r6jkq - static pods, start kubelet, recovery ReplicaSet.
2. etcd-minikube - pod for base, start from binary file or with kube-api-server, recovery Replication Controller.
3. ingress-nginx-controller-799dcd5d57-2kq8f - start from manifest, recovery ReplicaSet.
4. kube-apiserver-minikube - static pods, start kubelet, recovery Replication Controller.
5. kube-controller-manager-minikube - static pods, start kubelet, recovery Replication Controller.
6. kube-proxy-7l6k8 - static pods, start kubelet, recovery Replication Controller.
7. kube-scheduler-minikube - static pods, start kubelet, recovery Replication Controller.
8. storage-provisioner - start minikube, restart minikube for recovery.


HW 4-2
Steps:
1. git clone ....
2. minikube addons enable ingress
3. kubectl apply -f .
4. Check our deployments:
5.1 curl minikube.minikube - only deployment
5.2 curl -H "canary: never" minikube.minikube - only deployment
5.2 curl -H "canary: always" minikube.minikube - only canary

