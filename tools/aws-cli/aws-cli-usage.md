# AWS CLI Usage

## Resources 
## AWS CLI Command Reference:
https://docs.aws.amazon.com/cli/latest/index.html

## AWS CLI EKS:
https://docs.aws.amazon.com/cli/latest/reference/eks/index.html

## Aws eks commands:

List eks clusters:
```sh
$ aws eks list-clusters
```

Describe cluster:
```sh
$ aws eks describe-cluster --name "EKS-course-cluster"
```

Create a new eks cluster:

### Pre-requisite:
Use cloudformation to create a new vpc, subnet, sec group.

```sh
$ aws eks create-cluster --name EKS-by-cli --role-arn arn:aws:iam::351073549249:role/EKS-course-role --resources-vpc-config subnetIds=subnet-01568520d0e9c3934,subnet-01568520d0e9c3934,subnet-072e08d3abcfc863c,securityGroupIds=sg-050399a6d7e502406
```

`Note that aws eks can only create the EKS control plane, but you will still need to create the work nodes separately, by cloudformation.`

Delete cluster:
```sh
$ aws eks delete-cluster --name EKS-by-cli
```