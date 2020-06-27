Make sure the port for the kube-apiserver is correct. 

Change port from 2379 to 6443.


Run:

kubectl cluster-info --kubeconfig /root/admin.kubeconfig
