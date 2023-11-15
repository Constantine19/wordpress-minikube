# minikube Setup

## Intro
minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes. Using Minikube is the quickest way to spin up a single-node Kubernetes cluster with minimum maintenance.

## Note

This tutorial is based on Mac OS with M1 chip. For other acrhitectures, use the following [download link](https://minikube.sigs.k8s.io/docs/start/).

## Steps

1. Run the following command in your terminal to install the latest minikube (ARM64 macOS in this case):
    ```
    curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64
    sudo install minikube-darwin-arm64 /usr/local/bin/minikube
    ```

2. Start your cluster by running the following command:
    ```
    minikube start
    ```

    You should see the following output:

    ```
        ➜  wordpress-minikube minikube start
    😄  minikube v1.31.2 on Darwin 13.5.1 (arm64)
    ✨  Using the docker driver based on existing profile
    👍  Starting control plane node minikube in cluster minikube
    🚜  Pulling base image ...
        > gcr.io/k8s-minikube/kicbase...:  404.50 MiB / 404.50 MiB  100.00% 17.59 M
    🔄  Restarting existing docker container for "minikube" ...
    🐳  Preparing Kubernetes v1.27.4 on Docker 24.0.4 ...
    🔗  Configuring bridge CNI (Container Networking Interface) ...
    🔎  Verifying Kubernetes components...
        ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
        ▪ Using image docker.io/kubernetesui/dashboard:v2.7.0
        ▪ Using image docker.io/kubernetesui/metrics-scraper:v1.0.8
    💡  Some dashboard features require the metrics-server addon. To enable all features please run:

        minikube addons enable metrics-server


    🌟  Enabled addons: storage-provisioner, default-storageclass, dashboard
    🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
    ➜  wordpress-minikube
    ```
3. Congragulations, you have successfully installed minikube! 

For more information about the ways to interact with your cluster, check out this [link](https://minikube.sigs.k8s.io/docs/start/)
