# GCP DevOps Project

[![Build Status](https://img.shields.io/github/workflow/status/imranark/gcp-devops-project/Build%20and%20Test)](https://github.com/imranark/gcp-devops-project/actions)

This repository contains a DevOps project that demonstrates the automation of software development and deployment processes on Google Cloud Platform (GCP). The project utilizes various tools and technologies to streamline workflows and enhance productivity.

## Project Overview

The project focuses on building, testing, containerizing, and deploying a web application on GCP. It includes the following components:

- **Application Code**: The source code of the web application resides in the `app` directory.

- **Jenkins Pipeline**: The Jenkins pipeline is defined in the `Jenkinsfile`. It orchestrates the build, test, and deployment processes.

- **Ansible Playbooks**: The `playbooks` directory contains Ansible playbooks for infrastructure provisioning and configuration management.

- **Terraform Configuration**: The `terraform` directory holds the Terraform configuration files for provisioning GCP resources.

## Getting Started

To use this project, follow these steps:

1. Clone the repository using the following command:
   ```
   git clone https://github.com/imranark/gcp-devops-project.git
   ```

2. Set up GCP credentials and authentication on your local machine.

3. Install the necessary dependencies:

   - **Jenkins**: Set up Jenkins and install the required plugins.
   - **Ansible**: Install Ansible on your local machine or the Jenkins server.
   - **Terraform**: Install Terraform on your local machine.

4. Configure the GCP project and modify the necessary files to match your project requirements.

5. Create a Jenkins pipeline and point it to the `Jenkinsfile` in this repository.

6. Customize the pipeline stages, environment variables, and additional configurations based on your project needs.

7. Run the Jenkins pipeline and monitor the build and deployment processes.

## Documentation

### Jenkins Pipeline

The Jenkins pipeline defines the build, test, and deployment processes for the web application. It consists of the following stages:

- **Clean Workspace**: Cleans the workspace before starting the build process.
- **Code Checkout**: Checks out the source code from the Git repository.
- **Build**: Builds the application using Maven.
- **Test**: Executes the application tests.
- **Containerize**: Creates a Docker image of the application.
- **Push to Container Registry**: Pushes the Docker image to the Google Container Registry.
- **Provision Infrastructure**: Uses Terraform to provision the necessary infrastructure on GCP.
- **Configure Infrastructure**: Configures the provisioned infrastructure using Ansible playbooks.
- **Deploy**: Deploys the application on GCP.
- **Cleanup**: Cleans up the workspace and resources.

### Ansible Playbooks

The Ansible playbooks in the `playbooks` directory automate infrastructure provisioning and configuration management tasks. They include the following playbooks:

- **create_instance.yml**: Provisions a virtual machine instance on GCP.
- **configure_instance.yml**: Configures the provisioned instance by installing dependencies and setting up the necessary environment.
- **deploy_application.yml**: Deploys the web application on the provisioned instance.

Refer to the individual playbook files for detailed instructions on their usage and configuration.

### Terraform Configuration

The `terraform` directory contains the Terraform configuration files for provisioning the GCP resources. It includes:

- **main.tf**: Defines the main Terraform configuration, including the GCP provider, networking, and instance resources.
- **variables.tf**: Declares the input variables used in the Terraform configuration.
- **terraform.tfvars**: Contains the variable values specific to your project.

Please refer to the respective files for

 further information on their usage and customization.
