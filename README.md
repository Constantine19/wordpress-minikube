# WordPress Deployment on Minikube

This guide will walk you through each step of the process to create a local  environment for deploying WordPress on Kubernetes using Minikube.

## Requirements

Before you begin, make sure you have the following prerequisites installed on your machine:

- minikube — `v1.31.2`
- kubectl — `v1.27.2`
- Your favorite text editor — I use VS Code

## Step-by-Step Guide

Follow these steps to set up your WordPress lab environment:

1. [Install minikube](./docs/01-minikube-setup.md)
2. [Install kubectl](./docs/02-kubectl-setup.md)
3. [Deploy Secret](./docs/03-secret-deployment.md)
4. [Deploy MySQL](./docs/04-mysql-deployment.md)
5. [Deploy WordPress](./docs/05-wordpress-deployment.md)
6. [Verify Deployments](./docs/06-verify-deployments.md)
7. [Ship Logs to Elastic](./docs/07-ship-logs-to-elastic.md)

### Step 1: Install minikube

To create a local Kubernetes cluster, you'll need to install minikube. Follow the installation instructions as described here:

[Install minikube](./docs/01-minikube-setup.md)

### Step 2: Install kubectl

Kubectl is the command-line tool for interacting with Kubernetes clusters. Follow the installation instructions as described here:

[Install kubectl](./docs/02-kubectl-setup.md)

### Step 3: Secret Deployment

A Secret is an object that contains sensitive data such as a password, a token or a key. Such information might  be put in a Pod specification or in a container image. Follow the below instruction to create a simple kustomization.yaml file and deploy secret:

[Deploy Secret](./docs/03-secret-deployment.md)

### Step 4: Deploy MySQL

In this step, we will deploy a MySQL database on your Minikube cluster. Create a Kubernetes Deployment and Service for MySQL using the provided YAML file.

[Deploy MySQL](./docs/04-mysql-deployment.md)

### Step 5: Deploy WordPress

Now, let's deploy WordPress on your Minikube cluster. Create a Kubernetes Deployment and Service for WordPress using the provided YAML file.

[Deploy WordPress](./docs/05-wordpress-deployment.md)

### Step 6: Verify Deployments

Let's verify the status of the deployments for the WordPress on your Minikube cluster.

[Verify Deployments](./docs/05-wordpress-deployment.md)

### Step 7: Ship Logs to Elastic

In this step, you can set up log shipping to Elastic Cloud to monitor and analyze your WordPress application's logs.

[Ship Logs to Elastic](./docs/07-ship-logs-to-elastic.md)


## Issues and Troubleshooting

Below are some of the issues that I have encountered while seting up this lab:
1. [Error validating kustomization.yaml](./docs/08-error-validating-kustomization-file.md)
2. [Error establishing a database connection](./docs/09-db-connection-error.md)

## Conclusion

You have successfully set up a lab environment with WordPress running on Kubernetes using Minikube. You can now start experimenting and developing your WordPress application locally.
