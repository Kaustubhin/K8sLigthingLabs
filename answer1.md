Master Node:
kubectl drain node master --ignore-daemonsets
apt-get install kubeadm=1.17.0-00
kubeadm  upgrade plan v1.17.0
kubeadm  upgrade apply v1.17.0
apt-get install kubelet=1.17.0-00
kubectl uncordon master
kubectl drain node01 --ignore-daemonsets


Node01:
apt-get install kubeadm=1.17.0-00
kubeadm upgrade node --kubelet-version v1.17.0
apt-get install kubelet=1.17.0-00


Back on Master:
kubectl uncordon node01
kubectl get pods -o wide | grep gold (make sure this is scheduled on master node)
