# Assigment 3 - Kubernetes - How to run

## Step 1 - Navigate to Assignment Directory

Change directory to the assignment3 folder:

```
cd assignment3
```

## Step 2 - Start Minikube

```
minikube start
```

![alt text](/assignment3/images/image1.png)

## Step 3 - Enable the ingress add-on for Minikube

```
minikube addons enable ingress
```

## Step 4 - Deploy Kubernetes Configurations

Apply all Kubernetes configuration files:

```
kubectl apply -f .
```

![alt text](/assignment3/images/image2.png)

## Step 5 - Check Deployment Status

Verify that all pods are running:

```
kubectl get pods
```

![alt text](/assignment3/images/image3.png)

## Step 6 - Check Service Status

Ensure that services are created:

```
kubect get svc
```

![alt text](/assignment3/images/image4.png)

## Step 7 - Test NGINX Load Balance

Make requests to the NGINX service using curl.

```
curl http://$(minikube ip)/
```

We can see the ratio of 70:30 between app-1 and app-2
![alt text](/assignment3/images/image5.png)

## Step 7 - Cleanup

```
minikube stop
minikube delete
```

![alt text](/assignment3/images/image6.png)
