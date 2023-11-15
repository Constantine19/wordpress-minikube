# Wordpress Deployment

## Intro
We will use Kubernetes resource files to create a Wordpress pod.

## Note
Similar to the MySQL deployment, it is important to use `PersistentVolumeClaim`.

## Steps
1. Navigate to the `wordpress-minikube` directory within the repo and open the file called `wordpress-deployment.yaml`.
2. Run the following command:

    ```
    kubectl apply -f wordpress-deployment.yaml 
    ```
    You should see the following output:
    ```
    ➜  wordpress-minikube git:(main) ✗ kubectl apply -f wordpress-deployment.yaml 
    service/wordpress created
    persistentvolumeclaim/wp-pv-claim created
    deployment.apps/wordpress created
    ```
3. Congratulations, you have deployed your WordPress!
