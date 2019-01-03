# Kubernetes hello world

Created for an Axbit University session

### Run app
- Create a GCloud project (e.g. free trial), install gcloud SDK
- Create a Kubernetes cluster on Google Cloud Platform (micro instances are fine)
- `gcloud container clusters get-credentials --zone REGION CLUSTER_NAME`
- `kubectl apply -f webapp-deployment.yaml`
- `kubectl apply -f webapp-service.yaml`
- Use `kubectl get {pods,deployments,services}` or GCloud web console to inspect status
- Expose public IP by changing `webapp-service.yaml` to type LoadBalancer
- Change image of `webapp-deployment.yaml` to httpd, look at changes
- Can also roll back with `kubectl rollout undo deployments/webapp-deployment`

