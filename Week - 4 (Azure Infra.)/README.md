# Week-4 - Azure Infrastructure
# Azure Networking and Load Balancer Setup

This project demonstrates how to set up a comprehensive Azure networking environment, including VNets, subnets, VMs, load balancers, and an application gateway.

## A. Create a VNet with 2 Subnets

### Steps:
1. **Create a Virtual Network (VNet).**
2. **Create two subnets within the VNet:**
   - **Subnet-1:** Deploy a Linux VM and a Windows VM.
   - **Subnet-2:** Deploy an SQL Database.

**Resources:**
- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

## B. Create 4 VNets and Configure Hub and Spoke Architecture

### Steps:
1. **Create the following VNets:**
   - Management VNet (HUB)
   - Production VNet
   - Testing VNet
   - Developing VNet

2. **Configure Hub and Spoke Architecture:**
   - Link the Production, Testing, and Developing VNets as spokes to the Management VNet (HUB).
   - Launch a VM in each VNet.
   - Verify connectivity by pinging from the Management VM to every other VM.

**Resources:**
- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

## C. Create and Test Load Balancers

### Steps:
1. **Create an Internal Load Balancer.**
2. **Create an External Load Balancer.**
3. **Verify their functionality.**

**Resources:**
- [Azure Load Balancers - YouTube](https://www.youtube.com/watch?v=T7XU6Lz8lJw)
- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

## D. Create and Test Azure Application Gateway

### Steps:
1. **Create an Azure Application Gateway.**
2. **Test its functionality.**

**Resources:**
- [Azure Application Gateway - YouTube](https://www.youtube.com/watch?v=B3O6bXu-NbM)
- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)

## Verification

- Ensure the Hub and Spoke architecture is correctly configured by verifying connectivity.
- Test the Internal and External Load Balancers to ensure they are distributing traffic as expected.
- Test the Azure Application Gateway to ensure it is routing traffic correctly.

This setup provides a robust and scalable Azure network architecture suitable for various environments, including management, production, testing, and development.
