# CloudFormation - Cluster Creation

## Summary:
This section shows how to create a control plane and worker nodes with aws CloudFormation templates.

### Pre-requisites:
- All steps in the /initial-aws/setup should be completed before proceeding.


### Create VPC & Subnets Infrastructure:
- create-vpcs.md

### Create Kubernetes Control Plane:
- create-control-plane.md 
- Create new CloudFormation stack for the K8 control plane, which creates the VPC, Subnets, Security Group.
- Use /cloudformation/eks-course-vpc.yaml
- Update Description, VPC and subnet ip address ranges as needed.

### Create Kubernetes Worker Nodes: 
- launch-work-nodes.md
- Create new CloudFormation stack for the K8 worker nodes, which creates EC2 instances for the worker nodes.
- Use /cloudformation/eks-nodegroup.yaml
- Update ami, refer to https://docs.aws.amazon.com/eks/latest/userguide/eks-optimized-ami.html for the latest available amis based on Kubernetes version, region, etc.


### Additional Notes:
As of this writing, the use of EKSCTL to create an EKS cluster is more simplistic.  