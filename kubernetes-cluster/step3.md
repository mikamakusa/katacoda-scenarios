Once Kubernetes is installed, I invite you to initialize your cluster with the following command :  
`
kubeadm init --token 102952.1a7dd4cc8d1f4cc5
`

And install a pod network (aka : network overlay) : 
`
export kubever=$(kubectl version | base64 | tr -d '\n')
kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$kubever"
`


