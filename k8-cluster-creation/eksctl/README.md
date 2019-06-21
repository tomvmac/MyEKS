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

```sh
$ eksctl create cluster --region us-west-2 --name eksctl-test
```