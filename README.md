# devops-hw13 (!!! yet under development !!!)

### Build and Depoly an application on AWS EC2 resources by Ansible

Simple Tomcat application based on the test project:

[https://github.com/LovingFox/boxfuse-sample-java-war-hello.git](https://github.com/LovingFox/boxfuse-sample-java-war-hello.git)

##### Files

1. *ansible.cfg* (Ansible playbook)
1. *aws_ec2.yml* (Ansible AWS plugin config)
1. *build-and-deploy.yml* (Main Ansible playbook)
1. *instance_builder/* (Ansible role for EC2 Builder instance creation/removing)
1. *instance_webserver/* (Ansible role for EC2 Webserver instance creation/removing)
1. *builder/* (Ansible role for Builder vm)
1. *webserver/* (Ansible role for Builder vm)

##### Usage

1. Download repository

    ```bash
    git clone https://github.com/LovingFox/devops-hw13.git
    cd devops-hw13
    ```

1. Set AWS credentials

    ```bash
    export AWS_ACCESS_KEY="<your AWS access key>"
    export AWS_SECRET_KEY="<your AWS secret key>"
    ```

1. Start EC2 Instances (Builder and Webserver), Build an artifact and Depoly it

    ```bash
    ansible-playbook build-and-deploy.yml --tags up
    ```

1. Destroy EC2 Instances of Builder and Webserver

    ```bash
    ansible-playbook build-and-deploy.yml --tags down
    ```
