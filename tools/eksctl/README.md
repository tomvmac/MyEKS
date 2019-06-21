# EKSCTL

## WeaveWorks EKSCTL:
- Written in Go
- Enhanced feature set
- Can create underlying infrastructure (VPC, Subnets, SG)
- Creates EBS storageclass by default
- Can create and scale worker nodes in ASG


### EKSCTL Installation:
https://github.com/weaveworks/eksctl/releases

- Install eksctl and add to system path


### EKSCTL Getting Started Guide:
https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html


### Commands:

Get clusters:
```sh
$ eksctl get clusters
$ eksctl get cluster --name EKS-course-cluster
```

Create eks cluster:
```sh
$ eksctl create cluster --region us-west-2 --name eksctl-test
```

`Note that under the hood, this create cluster actually will create two cloudformation stacks, one to create the control plane and the other to create the worker nodes.`


Scale work nodes:
```sh
$ eksctl scale nodegroup --name eksctl-test --nodes=4 --region=us-west-2
```

Delete cluster:
https://docs.aws.amazon.com/eks/latest/userguide/delete-cluster.html

```sh
$ eksctl delete cluster --name eksctl-test --region=us-west-2
```