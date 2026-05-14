# Redis
Note:  image: redis  # this is image pulled from internet, not customized.

We use bastion host as Docker server and EKS client.
Make sure `aws configure` is done in bastion and connected to EKS cluster.

```
aws eks update-kubeconfig --region us-east-1 --name roboshop-dev
```
```
kubectl create namespace roboshop
```

```
git clone https://github.com/Lingaiahthammisetti/13.9.roboshop-redis.git
```

```
cd 13.9.roboshop-redis/
```

```
helm upgrade --install redis . -n roboshop
```

```
kubectl get pods -n roboshop
```