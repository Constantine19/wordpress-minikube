# Secret Deployment

## Intro
Since WordPress stores it’s data on a MySQL database, we’ll need a secret in Kubernetes for the password. For the sake of this lab, we will be putting the password in clear-text in MySQL pod definition.


## Note
It is adviseble not to store the password in a cleartext like in the below example in production.

## Steps
1. Navigate to the `wordpress-minikube` directory within the repo and open the file called `kustomization.yaml`. Pay attention to the password key that has a value `password`.
It should look like this:
    ```
    ---
    apiVersion: v1
    kind: Secret
    metadata:
        name: mysql-pass
    type: Opaque
    data:
        password: password
    ```
2. Run the following command:
    ```
    kubectl apply -f kustomization.yaml
    ```
    You should see the following output:
    ```
    ➜  wordpress-minikube git:(main) kubectl apply -f kustomization.yaml
    secret/mysql-pass created
    ```
3. Congratulations, you have created and deployed your secret!
