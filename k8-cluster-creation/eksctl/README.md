## EKSCTL Cluster Creation
https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html


### Commands:
For installation and other commands such as delete cluster, see tools/eksctl/README.md.

Get clusters:
```sh
$ eksctl get clusters
$ eksctl get cluster --name EKS-course-cluster
```

Create eks cluster:
EKSCTL creates two stacks in Cloudformation, one for control plane and one for worker nodes.  This is the same as manual CloudFormation template execution, except there is fully automated.

Create node group specifying instance size:
https://eksctl.io/

```sh
$ eksctl create cluster --region us-east-2 --name my-eks
```

Create eks cluster with specific node instance type:
```sh
$ eksctl create cluster --region us-east-2 --name my-eks --node-type=t2.small
```