# Hello
```
pip install awscli --upgrade --user
```
Make an IAM user with AdministratorAccess 
```
aws configure
```

### macOS
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

```
brew tap weaveworks/tap
```

```
brew install weaveworks/tap/eksctl
```
```
brew upgrade eksctl && brew link --overwrite eksctl
```
```
eksctl version
```

```
export CLUSTER_NAME="<your cluster name>"
export AWS_REGION="<your region>"
```


```
eksctl create cluster --name ${CLUSTER_NAME} --version 1.14 --region ${AWS_REGION} --fargate
```



```
eksctl utils associate-iam-oidc-provider --cluster ${CLUSTER_NAME} \
    --region ${AWS_REGION} --approve
```

```
aws eks describe-cluster --name ${CLUSTER_NAME} --region ${AWS_REGION} \
    --query cluster.identity.oidc.issuer --output text
```
```
aws iam create-role --role-name <rolename> --assume-role-policy-document file://trust.json --output=text
```
```
aws iam attach-role-policy --role-name <rolename>  --policy-arn arn:aws:iam::aws:policy/AmazonSageMakerFullAccess
```
```
kubectl apply -f installer.yaml
```
```
kubectl get crd | grep sagemaker
```
```
kubectl -n sagemaker-k8s-operator-system get pods
```
```
kubectl apply -f xgboost-mnist-trainingjob.yaml
```
```
kubectl get trainingjob
```


## References
https://aws.amazon.com/ko/blogs/machine-learning/introducing-amazon-sagemaker-operators-for-kubernetes/
https://eksworkshop.com/030_eksctl/launcheks/
https://sagemaker.readthedocs.io/en/stable/amazon_sagemaker_operators_for_kubernetes.html
