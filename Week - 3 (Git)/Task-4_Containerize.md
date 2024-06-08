# Create Azure Container Registry (ACR) and Deploy a Container from ACR

This guide will walk you through creating an Azure Container Registry (ACR), pushing an image to the ACR, and deploying a container from it.

## Prerequisites

- Azure account
- Docker installed on your local machine
- Azure CLI installed on your local machine

## Step-by-Step Guide

### 1. Create Azure Container Registry (ACR)

1. Open Azure Portal and navigate to "Create a resource".
2. Search for "Container Registry" and select it.
3. Click on "Create" and fill in the required details:
   - Subscription: Your subscription
   - Resource Group: Select an existing one or create a new one
   - Registry Name: `myacrregistry`
   - Location: Select your preferred location
   - SKU: Basic

4. Click "Review + create" and then "Create".

### 2. Login to ACR

1. Open your terminal and login to your Azure account:

    ```sh
    az login
    ```

2. Login to your Azure Container Registry:

    ```sh
    az acr login --name myacrregistry
    ```

### 3. Build and Push Docker Image to ACR

1. Build your Docker image:

    ```sh
    docker build -t myacrregistry.azurecr.io/myapp:v1 .
    ```

2. Push the image to your ACR:

    ```sh
    docker push myacrregistry.azurecr.io/myapp:v1
    ```

### 4. Create a Container Instance from ACR

1. Create a container instance using the image from your ACR:

    ```sh
    az container create --resource-group <YourResourceGroup> --name mycontainer --image myacrregistry.azurecr.io/myapp:v1 --cpu 1 --memory 1 --registry-login-server myacrregistry.azurecr.io --registry-username <ACRUsername> --registry-password <ACRPassword> --dns-name-label myappdns --ports 80
    ```

    Replace `<YourResourceGroup>`, `<ACRUsername>`, and `<ACRPassword>` with your actual resource group name, ACR username, and ACR password.

### 5. Verify the Deployment

1. Open your web browser and navigate to `http://myappdns.<region>.azurecontainer.io` (replace `<region>` with your actual region).
2. You should see your application running.

## Conclusion

You have successfully created an Azure Container Registry, pushed a Docker image to it, and deployed a container instance from that image. For more detailed information, refer to the official [Azure documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview).

## Resources

- [Azure Virtual Network Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Deploy a Container Instance from ACR](https://www.youtube.com/watch?vhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
