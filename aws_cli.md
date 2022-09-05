# Create a vpc using AWS cli

## Manage role-based access control (RBAC)

Doc: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example.html

<details><summary>Solution</summary>
<p>

vpc_id=`aws ec2 create-vpc --cidr-block 10.0.0.0/16 --query Vpc.VpcId --tag-specifications 'ResourceType=vpc,Tags=[{Key=name,Value=my-vpc}] --output text`
