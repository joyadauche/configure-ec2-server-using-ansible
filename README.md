# Goal
Install and configure docker, docker-compose on ec2 instances

# Pre-requisites
- [Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html%5D)
- [Configure AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html#cli-configure-files-using-profiles)
- Generate key pair for ec2 instances
- Launch ec2 instances in AWS with the generated key pair
- In **inventory_aws_ec2.yaml**, enter the following AWS account
    - profile you want ansible to use to connect to AWS
    - region where you launched the ec2 instances
- In **ansible.cfg**, enter the path to the key pair file created for the **private_key_file** property

# Run
- `ansible-playbook -i inventory_aws_ec2.yaml docker.yaml` to execute playbook
- `ansible-inventory inventory_aws_ec2.yaml --list` to show the inventory