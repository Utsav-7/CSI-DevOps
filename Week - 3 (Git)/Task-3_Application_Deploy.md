# Deploy a Web App on Azure App Service

This guide will walk you through creating an App Service Plan, provisioning a Web App in the existing App Service Plan, and deploying a simple welcome page.

## Prerequisites

- Azure account
- Basic knowledge of Azure Portal

## Step-by-Step Guide

### 1. Create an App Service Plan

1. Go to the [Azure Portal](https://portal.azure.com/).
2. Navigate to "Create a resource" and select "App Service Plan".
3. Fill in the required details:
   - Name: `MyAppServicePlan`
   - Resource Group: Select an existing one or create a new one
   - Operating System: Windows or Linux (depending on your preference)
   - Region: Select your preferred region
   - Pricing tier: Select an appropriate pricing tier (e.g., F1 Free)

4. Review and create the App Service Plan.

### 2. Provision a Web App in the Existing App Service Plan

1. Go to "Create a resource" and select "Web App".
2. Configure the basics:
   - Name: `MyWebApp`
   - Publish: Code
   - Runtime stack: Select your preferred runtime stack (e.g., .NET, Node.js, Python)
   - Operating System: Select the same OS as your App Service Plan
   - Region: Select the same region as your App Service Plan
   - App Service Plan: Select `MyAppServicePlan`

3. Review and create the Web App.

### 3. Deploy a Simple Welcome Page

#### Option 1: Using Azure Portal

1. Go to the Azure Portal and navigate to your Web App (`MyWebApp`).
2. In the left menu, select "Advanced Tools" and click "Go".
3. In the Kudu service, select "Debug console" -> "CMD".
4. Navigate to `site/wwwroot` and create an `index.html` file with the following content:

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Welcome</title>
    </head>
    <body>
        <h1>Welcome to My Web App!</h1>
    </body>
    </html>
    ```

5. Save the file and exit the Kudu service.

#### Option 2: Using GitHub

1. Create a new repository on GitHub and add the following `index.html` file to the repository:

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Welcome</title>
    </head>
    <body>
        <h1>Welcome to My Web App!</h1>
    </body>
    </html>
    ```

2. Go to the Azure Portal and navigate to your Web App (`MyWebApp`).
3. In the left menu, select "Deployment Center".
4. Select "GitHub" as the source, and authorize Azure to access your GitHub account.
5. Select your repository and branch, then configure and save the settings.

### 4. Verify the Deployment

1. Go to the Azure Portal and navigate to your Web App (`MyWebApp`).
2. Click on the URL provided to open your Web App in the browser.
3. You should see the welcome message: "Welcome to My Web App!"

## Conclusion

You have successfully created an App Service Plan, provisioned a Web App, and deployed a simple welcome page. For more detailed information, refer to the official [Azure documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview).

## Resources

- [Azure Virtual Network Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Deploy a Web App on Azure](https://www.youtube.com/watch?vhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
