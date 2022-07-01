# Lab Setup

## Test Cluster 1

Create GKE cluster using below gcloud command:

```shell 
 gcloud beta container clusters create test-cluster-1 \
 --zone=us-central1-a \
 --num-nodes=3 \
 --machine-type=n1-standard-1 \
 --disk-size=100 \
 --disk-type=pd-standard \
 --image-type=COS \
 --enable-autorepair \
 --enable-autoupgrade \
 --enable-autoscaling \
 --max-nodes=3 \
 --min-nodes=0 
```
 
 ### Test 1
 Deploy testapp-1 on test-cluster-1 
 ```
 kubectl create -f testapp-1.yaml
 ```
 
 ### Test 2
 Deploy testapp-2 on test-cluster-1
 ```
 kubectl create -f testapp-2.yaml
 ``` 
 
 ### Test 3
 Deploy testapp-3 on test-cluster-1
 ```
 kubectl create -f testapp-3.yaml
 ``` 
 ## Test Cluster 2
 
 Create GKE cluster using below gcloud command:
 
```shell
gcloud beta container clusters create test-cluster-2 \
 --cluster-version=1.12.8-gke.10 \
 --zone=us-west2-a \
 --node-version=1.12.8-gke.10 \
 --num-nodes=3 \
 --machine-type=n1-standard-4 \
 --disk-size=100 \
 --disk-type=pd-standard \
 --image-type=COS \
 --enable-autorepair \
 --enable-autoupgrade \
 --enable-autoscaling \
 --max-nodes=50 \
 --min-nodes=0
 ```
 
 ### Test 4
 Deploy testapp-4 on test-cluster-2
 ```
 kubectl create -f testapp-4.yaml
 ```
