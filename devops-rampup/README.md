# DevOps Ramp-up Projects

Welcome to the Endava Buenos Aires DevOps Ramp Up site. DevOps has a wide variety of practices, tools and methodologies which enable us to be an important part of and agile delivery culture. Most of the DevOps practitioners are part of the Continuous Delivery Practice. More info on the practice can be found here:

https://conf.endava.com/display/CDP/Continuous+Delivery+Practice

https://weblog.endava.com/continuous-delivery-initiative/introduction-to-cd/

This ramp-up is presented in challenges. Each challenge is chose to show new joiners the basics in some of the DevOps practices, and it is designed to help us use the same language after its completion. We are tool agnostics, so you can use any tool you like, but we do have a client base that need us to be proficient in some basic AWS concepts. They are ordered according our current view of projects necessities.


## Challenges

In challenges 1 to 3, you will have to set up the Source Code Management tool and branching methodologies, set up cloud based environments for the application and  gain experience with iaC tools. All challenges are meant to use the same application.

Challenges 4 and 5 build upon your pipeline to include more practices. These ones are more open for you to choose the tool stack of your preference.

### 0. Linux Basics
There are a lot of things to know and learn about Linux. For this reason, this challenge would be split in two parts:

***EDX COURSE:*** Please register at edX and enroll into the Introduction to Linux course. After that, complete the following chapters:
https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS101x+1T2020/home

- Linux Philosophy and Concepts
- Linux Basics and System Startup
- Command Line Operations
- Finding Linux Documentation
- Processes
- File Operations
- Text Editors
- User Environment
- Manipulating text
- Network Operations
- Bash Shell Scripting I
- Bash Shell Scripting II
- Local Security Principles

### 1. SCM: Set up git-flow

The objective of this challenge is to set up git-flow on a bitbucket repository. You will be provided with access to create the branch strategy you need.

 - Clone the repo and create **n FIXME** branches

```bash
git clone https://github.com/GeorgeMP388/ramp-up-app.git
```
To complete the challenge, create a branching strategy, provide a diagram of how the git flow works and the commands needed to interact to it for each actor in a software delivery team (developer, design lead, tester)


### 2. Cloud Environment

The objective of this challenge is to set up the cloud environment on which the application will run, whether is Azure, AWS or GCP. To complete this challenge, create the environments to run the application you cloned in the last environment.

There are 2 setups. Create at least the first one to complete the Challenge.

### AWS SetUp 1

![alt text][awslogo1]

[awslogo1]:AWSSetup3.png "AWSFirstSetUp"

Some of the steps needed:

  - Create an AWS account.
  - Setup a custom VPC.
  - Create a public and a private VPC.
  - Create route tables.
  - Setup a connection to internet (Internet Gateway and NAT).
  - Create ACL ans SG's (Security).
  - Setup an EC2 instances.

#### AWS SetUp 2
In case you already have some knowledge on AWS basics, this setup is meant to create a high availability architecture. This one is optional.
  ![alt text][awslogo2]

 [awslogo2]:https://github.com/GeorgeMP388/ramp-up-app/blob/main/devops-rampup/AWSSetup2.png "First SetUp"

Additional steps for this setup.
  - Setup an Elastic Load Balancer.
  - Create a new subnet in a different availability zone.
  - Set up a DMZ with a proxy server (Nginx is recommended).
  - Use RDS service to create a read replica in one of the AZs.


### 3. Infrastructure as a code

To complete this challenge, choose tool and create the necessary scripts to automate the provisioning of the environments for the application.

### 4. Containerization
To complete this challenge, create registry, dockerfiles and images for the installed apps.

### 5. Orchestration and clustering
***Deploy the applicaction in a k8s cluster***

Some of the steps needed:

- Package the application into a Docker image
- Upload the Docker image to Artifact Registry (optional)
- Create/setup a Kubernetes Cluster, tools to use: kubeadm, kubelet and kubectl
- Create all the require Services to deploy the app.
- Expose the app to the internet
- Deploy a new version of the app from the pipeline. (optional CI/CD)

Notes: 
*Use Secrets and config maps to handle the configurations*
*Make sure just the web app is exposed to the internet*
*No downtime in the deployments*


### Optional. Showcase challenge

If you still have time to spare, create your own challenge and show the rest of us the implementation of other DevOps dealings. Examples: Artifact Repository configuration, Test Automation Frameworks integration, Database deployment automation, packaging management automation, build scripting frameworks, release management tools, etc.

### Optional CI/CD

To complete this challenge, create all the Jenkins jobs needed to automate CI/CD on the newly created environment. Check the application folders create separate repos and deploy them automatically every time there's a new change in the code repository. If you feel like using a different CI tool, please do!

### optional Configuration Management

To complete this challenge, use any CM tool to automate the deployment of the application requirements in the newly created environment. See the 2 application folders in order to find out what are their dependencies. Some of the tools we use are Chef, Puppet, and Ansible.

