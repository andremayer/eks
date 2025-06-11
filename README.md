Some commands used:
```
docker build -t flask-hello-world:latest .
docker tag flask-hello-world:latest 655469961838.dkr.ecr.us-west-2.amazonaws.com/pocs:latest
docker push 655469961838.dkr.ecr.us-west-2.amazonaws.com/pocs:latest

aws eks list-clusters --region us-west-2
eksctl create cluster ^
  --name flask-demo-cluster ^
  --region us-west-2 ^
  --nodegroup-name standard-workers ^
  --node-type t3.medium ^
  --nodes 2 ^
  --nodes-min 1 ^
  --nodes-max 3
  
  
aws cloudformation describe-stacks --stack-name flask-demo-cluster --region us-west-2

aws eks update-kubeconfig --name flask-demo-cluster --region us-west-2

helm upgrade flask-app ./helm-chart
kubectl get pods
kubectl get services

kubectl logs flask-app-flask-app-76cd45c5f-7rfjj
```

![image](https://github.com/user-attachments/assets/fd81a3bf-8055-48eb-a01a-083d15bd495c)
