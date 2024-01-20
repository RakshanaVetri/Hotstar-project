# DevSecOps CI/CD: Deploying a Secure React Hotstar Clone 

**Date**: 6 January 2024  
**Author**: [Deepak Prasad](https://deepcoders-deepak-technical.vercel.app/)

## Overview

In the ever-evolving landscape of software development and deployment, the integration of robust security practices into the development pipeline has become imperative. DevSecOps, an amalgamation of Development, Security, and Operations, emphasizes the integration of security measures throughout the software development lifecycle, promoting a proactive approach to mitigate potential vulnerabilities and threats.

This blog, authored by Deepak Prasad, serves as a comprehensive guide to deploying a Hotstar clone—a popular streaming platform—using the principles of DevSecOps on Amazon Web Services (AWS). The deployment process encompasses the utilization of various tools and services, including Docker, Jenkins, Java, SonarQube, AWS CLI, Kubectl, and Terraform, to automate, secure, and streamline the deployment pipeline.

## GitHub Repository

[GITHUB](https://github.com/Aj7Ay/Hotstar-Clone.git)

## Prerequisites

- AWS account setup
- Basic knowledge of AWS services
- Understanding of DevSecOps principles
- Familiarity with Docker, Jenkins, Java, SonarQube, AWS CLI, Kubectl, Terraform, Docker Scout

## Step-by-Step Deployment Process

### Step 1: Setting up AWS EC2 Instance

1. Launch an EC2 instance with Ubuntu AMI, t2.large, and 30 GB storage.
2. Assign an IAM role with Admin access for learning purposes.

### Step 2: Installation of Required Tools on the Instance

Write and execute a script to automate the installation of:
- Docker
- Jenkins
- Java
- SonarQube container
- AWS CLI
- Kubectl
- Terraform

### Step 3: Jenkins Job Configuration

Create Jenkins jobs for:
- Creating an EKS cluster
- Deploying the Hotstar clone application

Configure Jenkins job stages:
- Sending files to SonarQube for static code analysis
- Running npm install
- Implementing OWASP for security checks
- Installing and running Docker Scout for container security
- Scanning files and Docker images with Docker Scout
- Building and pushing Docker images
- Deploying the application to the EKS cluster

### Step 4: Clean-Up Process

Remove the EKS cluster, delete the IAM role, and terminate the Ubuntu instance.

## Additional Steps for EC2 Instance and IAM Role Setup

### Step 1A: Setting up AWS EC2 Instance and IAM Role

1. Sign in to the AWS Management Console.
2. Navigate to the EC2 Dashboard and launch an instance as specified in Step 1.

### Step 1B: IAM Role

1. Search for IAM in the AWS console and click on "Roles."
2. Click on "Create Role," select entity type as AWS service, use case as EC2, and proceed with the role creation.

### Step 2: Installation of Required Tools on the Instance (Additional Scripts)

Execute scripts to install required tools for Java, Jenkins, Docker, Terraform, Kubectl, and AWS CLI.

## Jenkins Setup and Configuration

1. Access the Jenkins instance using the public IP.
2. Install suggested plugins and create an admin user.
3. Configure Sonar server and add quality gates.
4. Configure Docker credentials in Jenkins.

## Jenkins Job Configuration (Detailed Steps)

### Step 3A: EKS Provision Job

1. Install Terraform plugin in Jenkins.
2. Configure Terraform in Jenkins Tools.
3. Create a Jenkins job for EKS provisioning using a pipeline script.

### Step 3B: Hotstar Job

1. Install required plugins for Java, Sonar, Nodejs, OWASP, and Docker in Jenkins.
2. Configure global tool configuration for JDK, NodeJs, Sonarqube, Owasp, and Docker.
3. Configure Sonar server in Manage Jenkins.
4. Create Jenkins pipeline for Hotstar deployment with detailed stages.

### Pipeline Execution

1. Build the Jenkins pipeline.
2. Monitor the stage view for progress.
3. View detailed reports on SonarQube, OWASP, and Docker Scout.

### Step 4: Destruction

1. In Jenkins, run the Terraform-Eks job with parameters and the destroy action.
2. Wait for the EKS cluster to be deleted (approximately 10 minutes).
3. After deletion, remove the EC2 instance and IAM role.

## Conclusion

Congratulations on completing the journey of deploying your Hotstar clone using DevSecOps practices on AWS! This process has highlighted the power of integrating security measures seamlessly into the deployment pipeline, ensuring not only efficiency but also a robust shield against potential threats.

## Key Highlights

- Leveraging AWS services, Docker, Jenkins, and security tools for a secure and automated deployment pipeline.
- Implementing DevSecOps principles to fortify the application against vulnerabilities through continuous security checks.
- The seamless integration of static code analysis, container security, and automated deployment showcases the strength of DevSecOps methodologies.

## What’s Next?

Continue exploring the realm of DevSecOps and cloud technologies. Experiment with new tools, refine your deployment pipelines, and delve deeper into securing your applications effectively.
