REQUIREMENTS
===========

Install AWS CLI and Boto.

HOWTO
=====

    ansible-playbook playbooks/create-vpc.yml 

AWS
===

You'll need boto (python-boto on Debian, python2-boto on Arch) and access key id and secret and region from AWS exported:

    export AWS_ACCESS_KEY_ID=...
    export AWS_SECRET_ACCESS_KEY=...
    export region=..

WHY this repo?
=============
If you want to create a VPC in AWS with Public Subnet and Private Subnet and you are using NAT gateway instead of NAT instance, you can use this repo. Currently Ansible is working on the module ec2_vpc_nat_gateway however it is not production ready so I used AWS CLI for creating the NAT gateway.

VARIABLES
=========

You can see the variables on the var folder.

For eg:

``` 
cidr: 10.22.0.0/16
public_subnet: 10.22.0.0/24
private_subnet: 10.22.1.0/24
public_subnet_az: us-east-1b
private_subnet_az: us-east-1d
```

ADDITIONAL INFORMATION
======================
Add `-u <user>` to login with a name different than your local login-name (defaults in ansible.cfg).
Add `-l <host or group>` to limit the playbook to just that/those host(s).
Use `-e ansible_ssh_port` to change the ssh port used (defaults in ansible.cfg).

