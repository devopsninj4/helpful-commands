# VPC

## Create a vpc using aws cli

Links: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example.html

https://docs.aws.amazon.com/cli/latest/reference/ec2/create-vpc.html

https://brad-simonin.medium.com/create-an-aws-vpc-and-subnet-using-the-aws-cli-and-bash-a92af4d2e54b

<details><summary>Commands</summary>
<p>

```bash
vpc_id=$(aws ec2 create-vpc --cidr-block 10.0.0.0/16 --query Vpc.VpcId --tag-specifications \
  'ResourceType=vpc,Tags=[{Key=name,Value=my-vpc}] --output text)
```
