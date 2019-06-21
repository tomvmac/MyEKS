# AWS CLI Usage

## Resources 
## AWS CLI Command Reference:
https://docs.aws.amazon.com/cli/latest/index.html

## AWS CLI EKS:
https://docs.aws.amazon.com/cli/latest/reference/eks/index.html

## Aws eks commands:
// list eks clusters
$aws eks list-clusters

// describe cluster
$aws eks describe-cluster --name "EKS-course-cluster"

// create a new eks cluster

// pre-requisite is to use cloudformation to create a new vpc, subnet, sec group
Update eks-course-vpn.yaml

aws eks create-cluster --name EKS-by-cli --role-arn arn:aws:iam::351073549249:role/EKS-course-role --resources-vpc-config subnetIds=subnet-01568520d0e9c3934,subnet-01568520d0e9c3934,subnet-072e08d3abcfc863c,securityGroupIds=sg-050399a6d7e502406

Note that aws eks can only create the EKS control plane, but you will still need to create the work nodes separately, by cloudformation.

// delete cluster
aws eks delete-cluster --name EKS-by-cli
