# MySQL Deployment

## Intro
We will use Kubernetes resource files to create a MySQL database.

## Note
It is important to use `PersistentVolumeClaim` to make data persistent and `readinessProbe` and `livenessProbe` to ensure that MySQL pod will be considered healthy only if it is ready to accept connections on port `3306`.

## Steps
1. Navigate to the `wordpress-minikube` directory within the repo and open the file called `mysql-deployment.yaml`.
2. Run the following command:

    ```
    kubectl apply -f mysql-deployment.yaml 
    ```
    You should see the following output:
    ```
    ➜  wordpress-minikube git:(main) ✗ kubectl apply -f mysql-deployment.yaml 
    service/wordpress-mysql created
    persistentvolumeclaim/mysql-pv-claim created
    deployment.apps/wordpress-mysql created
    ```
3. Congratulations, you have deployed your MySQL database!
