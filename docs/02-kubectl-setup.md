# kubectl Setup

## Intro
kubectl is a tool that allows you to run commands against Kubernetes clusters. You can use kubectl to deploy applications, inspect and manage cluster resources and view logs. 

## Note

This tutorial is based on Mac OS with M1 chip. Therefore, we will be using the Homebrew package manager that needs to be installed prior. The installation guide for Homebrew lives [here](https://brew.sh/).

## Steps

1. Run the following command in your terminal
    ```
    brew install kubectl
    ```
2. Run the following command to ensure that it is installed:
    ```
    kubectl version --client
    ```
    You should see the following output:
    ```
    Client Version: v1.27.2
    Kustomize Version: v5.0.1
    ```
3. Congragulations, you have successfully installed kubectl! 

For more information about the ways to install and use kubectl command within your cluster, check out this [link](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
