# ansible
Ansible deployment of docker containers to AWS EC2 instances


1. Playbook to deploy an EC2 instance on AWS (update instance_name manually)
Security group configured for EC2 deployment is whitelisted for 0/0 SSH access for ease of testing.

    Before you run this playbook, make sure to do the following:
    1. Create a public (.pub) and private key in the ~/.ssh/ directory
    ssh-keygen -t rsa -b 4096 -f ~/.ssh/ec2.key

    2. Ensure that private key is not publicly viewable
    chmod 400 ~/.ssh/ec2.key

2. Playbook that will deploy docker, docker-compose and rest of the files needed for Ansible to deploy the containers on AWS EC2 instances.
3. Separate playbooks for deployment of docker containers to Dev and Stage EC2 instances
