# devops-hw13 (!!! yet under development !!!)

### Build and Depoly an application on AWS EC2 resources by Ansible

Simple Tomcat application based on the test project:

[https://github.com/LovingFox/boxfuse-sample-java-war-hello.git](https://github.com/LovingFox/boxfuse-sample-java-war-hello.git)

##### Files

1. *ansible.cfg* (Ansible playbook)
1. *aws_ec2.yml* (Ansible AWS plugin config)

##### Usage

1. Download repository

    ```bash
    git clone https://github.com/LovingFox/devops-hw13.git
    cd devops-hw13
    ```

1. Prepare AWS EC2 key pair

    ```bash
    aws ec2 create-key-pair --key-name devops-hw13-key \
       --query 'KeyMaterial' --output text \
       > devops-hw13.key
    chmod 400 devops-hw13.key
    ```

1. Set AWS credentials

    ```bash
    export AWS_ACCESS_KEY="<your AWS access key>"
    export AWS_SECRET_KEY="<your AWS secret key>"
    ```

1. Launch the application

    ```bash
    ```
