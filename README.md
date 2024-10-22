# CloudFormation Template: EC2 Instances with Docker and Auto Scaling

This CloudFormation template creates multiple EC2 instances running Ubuntu, installs Docker, authenticates to Docker Hub, and distributes the instances across multiple subnets. Each instance is configured with an IAM role and an Auto Scaling Group for flexibility and scalability.

## Key Features:
- **Multiple EC2 Instances**: Specify the number of instances and distribute them across subnets.
- **Docker Installation**: Automatically installs Docker and logs into Docker Hub.
- **IAM Role**: Instances are assigned an IAM role for enhanced security and access control.
- **Auto Scaling**: Automatically adjusts the number of instances based on demand.
- **Security Group**: Allows SSH (port 22) and HTTP (port 80) access.

## Parameters:
- `InstanceType`: Specify EC2 instance type (e.g., t3.xlarge).
- `KeyName`: SSH access via an existing EC2 KeyPair.
- `VPCId`: VPC ID where instances will be launched.
- `SubnetIds`: Subnet IDs for distributing instances.
- `DockerHubUsername` & `DockerHubPassword`: Credentials to authenticate to Docker Hub.
- `InstanceCount`: Number of EC2 instances to create.
- `AMI`: Ubuntu AMI ID for the instances.

## Outputs:
- `AutoScalingGroupName`: Name of the created Auto Scaling Group.

This template simplifies deploying Dockerized applications at scale with minimal setup effort.
