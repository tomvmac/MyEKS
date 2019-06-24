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

Create eks cluster:
EKSCTL creates two stacks in Cloudformation, one for control plane and one for worker nodes.  This is the same as manual CloudFormation template execution, except there is fully automated.

Create node group specifying instance size:
https://eksctl.io/

```sh
$ eksctl create cluster --region us-east-2 --name my-eks
```

Create eks cluster with specific node instance type:
```sh
$ eksctl create cluster --region us-east-2 --name my-eks --node-type t2.small
```

`Note that under the hood, this create cluster actually will create two cloudformation stacks, one to create the control plane and the other to create the worker nodes.`


Scale work nodes:
```sh
$ eksctl scale nodegroup --name my-eks --nodes=4 --region us-east-2
```

Delete cluster:
https://docs.aws.amazon.com/eks/latest/userguide/delete-cluster.html

```sh
$ eksctl delete cluster --name my-eks --region us-east-2
```