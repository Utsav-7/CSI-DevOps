# Create Azure Container Instance and Deploy a Simple Docker Application

This guide will walk you through creating an Azure Container Instance, deploying a simple Docker application on it, creating container groups, and testing its functionality.

## Prerequisites

- Azure account
- Docker installed on your local machine
- Azure CLI installed on your local machine

## Step-by-Step Guide

### 1. Create a Simple Docker Application

1. Create a simple Docker application. For this example, we'll use a basic Nginx web server.

    ```dockerfile
    # Dockerfile
    FROM nginx:alpine
    COPY . /usr/share/nginx/html
    ```

2. Create a simple `index.html` file.

    ```html
    <!-- index.html -->
    <!DOCTYPE html>
    <html>
    <head>
        <title>Welcome to Azure Container Instance</title>
    </head>
    <body>
        <h1>Deployed with Azure Container Instance!</h1>
    </body>
    </html>
    ```

3. Build your Docker image:

    ```sh
    docker build -t mynginx:v1 .
    ```

### 2. Push Docker Image to Docker Hub

1. Tag your image:

    ```sh
    docker tag mynginx:v1 <your_dockerhub_username>/mynginx:v1
    ```

2. Push the image to Docker Hub:

    ```sh
    docker push <your_dockerhub_username>/mynginx:v1
    ```

### 3. Create an Azure Container Instance

1. Open your terminal and login to your Azure account:

    ```sh
    az login
    ```

2. Create a container instance using the image from Docker Hub:

    ```sh
    az container create --resource-group <YourResourceGroup> --name mycontainer --image <your_dockerhub_username>/mynginx:v1 --cpu 1 --memory 1 --dns-name-label mynginxapp --ports 80
    ```

### 4. Verify the Deployment

1. Open your web browser and navigate to `http://mynginxapp.<region>.azurecontainer.io` (replace `<region>` with your actual region).
2. You should see the welcome message from your Docker application.

### 5. Create Container Groups

1. Create a container group definition in a JSON file (e.g., `container-group.json`):

    ```json
    {
      "location": "eastus",
      "properties": {
        "containers": [
          {
            "name": "mynginx",
            "properties": {
              "image": "<your_dockerhub_username>/mynginx:v1",
              "resources": {
                "requests": {
                  "cpu": 1.0,
                  "memoryInGB": 1.5
                }
              },
              "ports": [
                {
                  "port": 80
                }
              ]
            }
          }
        ],
        "osType": "Linux",
        "ipAddress": {
          "type": "Public",
          "ports": [
            {
              "protocol": "tcp",
              "port": 80
            }
          ],
          "dnsNameLabel": "mynginxgroup"
        }
      }
    }
    ```

2. Create the container group:

    ```sh
    az container create --resource-group <YourResourceGroup> --file container-group.json
    ```

### 6. Test Container Group Functionality

1. Open your web browser and navigate to `http://mynginxgroup.<region>.azurecontainer.io` (replace `<region>` with your actual region).
2. You should see the welcome message from your Docker application.

## Conclusion

You have successfully created an Azure Container Instance, deployed a simple Docker application on it, created container groups, and tested its functionality. For more detailed information, refer to the official [Azure documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview).

## Resources

- [Azure Virtual Network Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Create and Deploy Container Instances](https://www.youtube.com/watch?vhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
