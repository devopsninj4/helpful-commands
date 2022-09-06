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
</p>
</details>

## Create vpc, subnets, internet gateway and route table
  
<details><summary>Commands</summary>
<p>

```bash
vpc_id=$(aws ec2 create-vpc --cidr-block 10.0.0.0/16 --query Vpc.VpcId --tag-specifications \
'ResourceType=vpc,Tags=[{Key=Name,Value=my-vpc}]' --output text)
 
public_subnet=$(aws ec2 create-subnet --vpc-id $vpc_id --cidr-block 10.0.1.0/24 --tag-specifications \
'ResourceType=subnet,Tags=[{Key=Name,Value=public_subnet}]' --output text)

private_subnet=$(aws ec2 create-subnet --vpc-id $vpc_id --cidr-block 10.0.2.0/24 --tag-specifications \
'ResourceType=subnet,Tags=[{Key=Name,Value=private_subnet}]' --output text)
  
igw_id=$(aws ec2 create-internet-gateway --query InternetGateway.InternetGatewayId --output text)
  
aws ec2 attach-internet-gateway --vpc-id $vpc_id --internet-gateway-id $igw_id

rt_id=$(aws ec2 create-route-table --vpc-id $vpc_id --query RouteTable.RouteTableId --tag-specifications \
'ResourceType=route-table,Tags=[{Key=Name,Value=public_rt}]' --output text)
  
aws ec2 create-route --route-table-id $rt_id --destination-cidr-block 0.0.0.0/0 \
--gateway-id $igw_id)
  
aws ec2 associate-route-table --subnet-id $public_subnet --route-table $rt_id
  
aws ec2 modify-subnet-attribute --subnet-id $public_subnet --map-public-ip-on-launch
```
</p>
</details>

  
## Filter subnet with the tag Name=public_subnet
  
<details><summary>Commands</summary>
<p>
  
```bash
aws ec2 create-route --route-table-id $rt_id --destination-cidr-block 0.0.0.0/0 \
--gateway-id $igw_id)
```
