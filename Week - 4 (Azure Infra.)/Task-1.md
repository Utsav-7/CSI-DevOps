# Task-1 : Networking Resources

## Resources

- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

## Tasks

### A. Create a Virtual Network (VNet) with 2 Subnets
1. **Subnet-1**: 
   - Linux VM
   - Windows VM
2. **Subnet-2**: 
   - SQL DB

### B. Create 4 VNets and Configure Hub and Spoke Architecture
1. **Management VNet (HUB)**
2. **Production VNet**
3. **Testing VNet**
4. **Development VNet**

#### Steps:
1. Launch a VM in each VNet.
2. Verify the Hub and Spoke architecture by pinging from the Management VM to every other VM.

### C. Create and Test Internal and External Load Balancers
- Follow the provided resources to create internal and external load balancers and test their functionality.

### D. Create and Test Azure Application Gateway
- Follow the provided resources to create and test the Azure Application Gateway.

### E. Set Up a Domain, Server on a VM, and Use DNS Server for Traffic
- Follow the provided resources to set up a domain, server on a VM, and configure the DNS server for traffic management.

## Detailed Steps

### 1. Create a VNet with Subnets

Refer to the [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview) for detailed instructions.

### 2. Create Hub and Spoke Architecture

Watch relevant tutorials and refer to documentation for step-by-step guidance on configuring the VNets.

### 3. Create Internal and External Load Balancers

Follow the relevant tutorials and documentation to set up and test load balancers.

### 4. Azure Application Gateway

Use the relevant resources to create and test the application gateway.

### 5. Domain and DNS Server Setup

Set up a domain and DNS server by following the relevant tutorials and documentation.

## Verification

- Ensure that the VM in each VNet can communicate with the Management VM.
- Test load balancing by simulating traffic to the internal and external load balancers.
- Verify the application gateway's functionality by routing traffic through it.
- Confirm the DNS server directs traffic appropriately to the server set up on the VM.

## Additional Information

- For more networking resources and tutorials, refer to Azure documentation and other relevant online resources.

