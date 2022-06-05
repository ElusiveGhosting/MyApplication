Setting Up Voting App:

kubectl create -f voting-app-deploy.yaml

kubectl create -f voting-service.yaml

kubectl create -f redis-deploy.yaml

kubectl create -f redis-service.yaml

kubectl create -f result-app-deploy.yaml

kubectl create -f result-service.yaml

kubectl create -f postgres-deploy.yaml

kubectl create -f postgres-service.yaml

kubectl create -f worker-app-deploy.yaml
