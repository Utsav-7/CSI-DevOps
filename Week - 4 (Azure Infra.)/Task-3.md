# Task-3 : Load Balancer Setup

## Resources

- [YouTube Tutorial on Load Balancers](https://www.youtube.com/watch?v)

## Tasks

### A. Create an Internal Load Balancer

1. **Steps**:
   1. Navigate to the Azure portal.
   2. Go to "Create a resource" and search for "Load Balancer".
   3. Choose "Internal" as the type of load balancer.
   4. Configure the backend pool with your VMs.
   5. Set up the health probes.
   6. Configure the load balancing rules.
   7. Review and create the internal load balancer.

### B. Create an External Load Balancer

1. **Steps**:
   1. Navigate to the Azure portal.
   2. Go to "Create a resource" and search for "Load Balancer".
   3. Choose "Public" as the type of load balancer.
   4. Configure the backend pool with your VMs.
   5. Set up the health probes.
   6. Configure the load balancing rules.
   7. Review and create the external load balancer.

### C. Test the Load Balancers

1. **Internal Load Balancer**:
   1. Use internal IP addresses to test the load balancer within the virtual network.
   2. Verify that the traffic is being distributed across the VMs in the backend pool.

2. **External Load Balancer**:
   1. Use the public IP address to test the load balancer from outside the virtual network.
   2. Verify that the traffic is being distributed across the VMs in the backend pool.

## Verification

- Ensure that the internal load balancer distributes traffic correctly within the virtual network.
- Verify that the external load balancer distributes traffic correctly from external sources.

## Additional Information

- Refer to the [YouTube Tutorial on Load Balancers](https://www.youtube.com/watch?v) for a step-by-step visual guide.
- Consult the Azure documentation for more detailed instructions and advanced configurations.
