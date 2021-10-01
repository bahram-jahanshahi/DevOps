# Create Kubernetes cluster on Amazon Eks by eksctl
This guid is base on a video on Youtube [AWS EKS - Create Kubernetes cluster on Amazon EKS | the easy way](https://www.youtube.com/watch?v=p6xDCz00TxU&t=58s) published by [TechWorld with Nana](https://www.techworld-with-nana.com/).  

## Install eksctl
### Mac OS

Notice that you should install aws cli first then have login to AWS by ``` aws config``` shell command.  
Follow this steps to install eksctl:  

1. Install the Weaveworks Homebrew tap.
```console
brew tap weaveworks/tap
```

2. Install eksctl
```console
brew install weaveworks/tap/eksctl
```
3. Test that your installation was successful with the following command.
```console
eksctl version
```

## Create Amazon EKS Cluster
```console
eksctl create cluster --name test-cluster --version 1.17 --region eu-north-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2 
```