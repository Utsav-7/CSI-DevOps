# Deploy Linux and Windows Virtual Machines on Azure

This guide will walk you through deploying Linux and Windows virtual machines (VMs) on Azure and accessing them using SSH and RDP.

## Prerequisites

- Azure account
- Basic knowledge of Azure Portal

## Step-by-Step Guide

### 1. Create a Virtual Network

1. Go to the [Azure Portal](https://portal.azure.com/).
2. Navigate to "Create a resource" and select "Virtual Network".
3. Fill in the required details:
   - Name: `MyVirtualNetwork`
   - Address space: `10.0.0.0/16`
   - Subnet name: `default`
   - Subnet address range: `10.0.0.0/24`
4. Review and create the virtual network.

For more information, refer to the [Azure Virtual Network documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview).

### 2. Deploy a Linux VM

1. Go to "Create a resource" and select "Virtual Machine".
2. Configure the basics:
   - Name: `MyLinuxVM`
   - Region: Select your preferred region
   - Image: `Ubuntu Server 20.04 LTS`
   - Size: Select a size based on your requirements
   - Authentication type: SSH public key
   - Username: `azureuser`
   - SSH public key: Paste your public key
3. Under the "Networking" tab, ensure that the VM is connected to `MyVirtualNetwork`.
4. Review and create the VM.

### 3. Deploy a Windows VM

1. Go to "Create a resource" and select "Virtual Machine".
2. Configure the basics:
   - Name: `MyWindowsVM`
   - Region: Select your preferred region
   - Image: `Windows Server 2019 Datacenter`
   - Size: Select a size based on your requirements
   - Authentication type: Password
   - Username: `azureuser`
   - Password: Create a strong password
3. Under the "Networking" tab, ensure that the VM is connected to `MyVirtualNetwork`.
4. Review and create the VM.

### 4. Accessing the VMs

#### Accessing the Linux VM using SSH

1. Open a terminal on your local machine.
2. Run the following command, replacing `your-public-ip` with the public IP address of your Linux VM:

    ```sh
    ssh azureuser@your-public-ip
    ```

#### Accessing the Windows VM using RDP

1. Open the Remote Desktop Connection application on your local machine.
2. Enter the public IP address of your Windows VM and click "Connect".
3. Enter the username `azureuser` and the password you created.

## Conclusion

You have successfully deployed Linux and Windows virtual machines on Azure and accessed them using SSH and RDP. For more detailed information, refer to the official [Azure Virtual Network documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview).

## Resources

- [Azure Virtual Network Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Deploy Linux VM on Azure](https://www.youtube.com/watch?vhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Deploy Windows VM on Azure](https://www.youtube.com/watch?vhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
