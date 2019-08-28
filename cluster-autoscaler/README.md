#Lab Setup

## Test 1

Create GKE cluster using below gcloud command:

gcloud beta container clusters create test-cluster-1 \
 --cluster-version=1.12.8-gke.10 \
 --zone=us-central1-a \
 --node-version=1.12.8-gke.10 \
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
 
 
