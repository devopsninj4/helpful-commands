# ANSIBLE

## Installation and upgrade

<details><summary>Links</summary>
<p>
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
</p>
</details>  
  
<details><summary>Install the ansible package</summary>
<p>

```bash
#Pip must be present before ansible installation
python -m pip install ansible
```

</p>
</details>

<details><summary>Upgrade the ansible package</summary>
<p>

```bash
#Pip must be present before ansible installation
python -m pip install --upgrade ansible
```

</p>
</details>

<details><summary>Check installed version</summary>
<p>

```bash
#ansible-core
ansible --version
```

```bash
#ansible
python -m pip show ansible
```

</p>
</details>

## Ad-hoc commands

<details><summary>Ping</summary>
<p>

```bash
#ping all hosts
ansible -m ping all
```

</p>
</details>

## Filter subnet with the tag Name=public_subnet

<details><summary>Commands</summary>
<p>
  
```bash
aws ec2 describe-subnets --filters Name=tag:Name,Values=public_subnet --query "Subnets[*].SubnetId" --output text
```
