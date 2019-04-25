# CloudComputing - Kubernetes

Deploy the web api on a VM using deploy_api.sh script.
Then, modify todolist.py using the external-ip address of the web service for the web app.

Create a Dockerfile for Flask web app.

Under the directory containing Docker file and all needed files for app, create a docker image:

docker build -t tdoan5/cs5550-demo .

Push the docker image to Docker hub using your docker account:
docker push tdoan5/cs5550-demo .

Create Kubernetes cluster using deploy_kubernetes.sh script.

LoadBalancer service will stays in pending status in about 30-60sec before getting the external-ip assigned. After 30s – 60s, we can call follow command to get external-ip and test the deployed app:

kubectl get service cc5550
