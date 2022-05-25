# Kubernetes Setup
 
Install minikube to windows 10

cd "C:\Users\King of Pirates\Documents\Kubernetes"

minikube start --vm-driver=hyperv  #create kubectl as an alias to minikube to use kubernetes

kubectl get nodes #returns the kubernetes cluster

kubectl get nodes -o wide #returns brief details about kubernetes cluster

kubectl get pods  #returns deployed docker containers(called as POD's w.r.t kubernetes)

kubectl run nginx --image=nginx #deploys a nginx POD

kubectl describe pods #returns brief description of POD

kubectl delete pod webapp #deletes a POD named "webapp"

kubectl create -f pod-definition.yaml #create POD as per definition

kubectl apply -f pod-definition.yaml #update created POD in previous step based on updated definition of file pod-definition.yaml

kubectl create -f replication-controller.yaml #create POD's as per definition as part of replication-controller

kubectl get replicationcontroller #return created replication-controller

kubectl create -f replica-set.yaml #create POD-Group as per definition as part of replica-set

kubectl get replicaset #return created replica-set

kubectl replace -f replica-set.yaml  #update replica-set based on new definition

kubectl scale --replicas=6 -f replicaset.yaml #update replica-set's number of replicas as well as the replica's themselves based on new definition

kubectl scale  replicaset myreplicaset --replicas=6 #update replica-set's number of replicas

kubectl describe replicateset setname #describe a replica-set file definition

kubectl edit replicaset resplicasetname #update replica-set by directly updating the file


