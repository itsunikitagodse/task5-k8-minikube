** Task 5 – Build a Kubernetes Cluster Locally with Minikube
**

This project demonstrates how to deploy and manage a containerized application locally using Kubernetes via Minikube on Windows.

 Tools Used

- [Minikube](https://minikube.sigs.k8s.io/docs/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Docker](https://www.docker.com/products/docker-desktop/)
- Windows 10/11

 Files Included

- `deployment.yml` – Kubernetes Deployment configuration for an Nginx app.
- `service.yml` – NodePort Service to expose the app on a local browser.
- `pods-services.png` – Screenshot showing running pods and services list.

**Steps to Run This Project Locally
**

1. Start Minikube

>> minikube start --driver=docker

2. Deploy the App

>> kubectl apply -f deployment.yaml

3. Expose the App as a Service

>> kubectl apply -f service.yaml

4. Check Resources

>> kubectl get pods
>> kubectl get services

 5. Access the App

>> minikube service nginx-service

 6. Scale the Deployment

>> kubectl scale deployment nginx-deployment --replicas=4

 7. Get Logs and Details

>> kubectl describe deployment nginx-deployment
>> kubectl logs <pod-name>

Screenshots attached

- pods-services.png
- deployment.png

 Output
After running minikube service nginx-service, the browser will open an Nginx welcome page on localhost. (refer image nginx.png)
