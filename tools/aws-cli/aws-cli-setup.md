# AWS CLI

## Summary
- Switch from manual setup to scripting
- Infrastructure as code
- Built upon Python
- Creates K8 control plane
- Requires existing AWS infrastructure (VPC, SG)


## AWS CLI Setup:


## Pre-requisites:
1. Install Python (Includes PIP)
    a. https://www.python.org/downloads/


## Install AWS CLI:
1. https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

```sh
$ pip3 install awscli --user
```

### Note:
Figure out aws path, see docs above and add folder to path

Check installation:
```sh
$ aws --version
```