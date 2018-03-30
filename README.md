# Telport AWS Quickstart Guide

AWS quickstart for teleport

## Development instructions

**To build an AMI**

```
make oss
```

Update oss.yaml with new AMI image IDs.

**Launch a dev cloudformation stack**

```
export STACK=test1
export STACK_PARAMS="ParameterKey=KeyName,ParameterValue=KeyName ParameterKey=DomainName,ParameterValue=teleport.example.com ParameterKey=DomainAdminEmail,ParameterValue=admin@example.com ParameterKey=HostedZoneID,ParameterValue=AWSZONEID"
make create-stack
```

