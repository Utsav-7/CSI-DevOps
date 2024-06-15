## A. Create a Vnet, 2 Subnets Subnet-1: Linux VM, WindowsVM Subnet-2: SQL DB, B. Create 4 VNets 1. Management Vnet (HUB) 2. Production Vnet 3. Testing Vnet 4. Developing Vnet And Configure Hub and Spoke Architecture and verify it's working by launching VM in each VNet and ping from Managemnent VM to every other VM
Resources :
https://www.youtube.com/watch?v=f7sTlsjcaxwhttps://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview

## Resources

- [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [YouTube Tutorial on Virtual Networks](https://www.youtube.com/watch?v=f7sTlsjcaxw)

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

## Detailed Steps

### 1. Create a VNet with Subnets

Refer to the [Azure Virtual Networks Overview](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview) for detailed instructions on creating a VNet and subnets.

### 2. Create Hub and Spoke Architecture

Follow the steps in the [YouTube Tutorial on Virtual Networks](https://www.youtube.com/watch?v=f7sTlsjcaxw) to create the following VNets and configure the Hub and Spoke architecture:

- Management VNet (HUB)
- Production VNet
- Testing VNet
- Development VNet

### 3. Verify Hub and Spoke Architecture

1. Launch a VM in each VNet (Management, Production, Testing, Developing).
2. From the Management VM, ping every other VM to ensure connectivity and verify the Hub and Spoke architecture is working correctly.

## Verification

- Ensure that the VMs in Subnet-1 and Subnet-2 within the same VNet can communicate with each other.
- Verify that the Management VM can ping the VMs in Production, Testing, and Development VNets.

## Additional Information

- For more networking resources and detailed guides, refer to the Azure documentation and relevant online tutorials.
