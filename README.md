# Hello
```
pip install awscli --upgrade --user
```

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
eksctl create cluster --name=eksworkshop-eksctl --nodes=3 --managed --alb-ingress-access --region=us-west-2
```


```
kubectl get nodes 
```














## References
https://eksworkshop.com/030_eksctl/launcheks/
