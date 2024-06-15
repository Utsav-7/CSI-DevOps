# Task-4 : Azure Application Gateway Setup

## Resources

- [YouTube Tutorial on Azure Application Gateway](https://www.youtube.com/watch?v=B3O6bXu-NbM)

## Tasks

### A. Create an Azure Application Gateway

1. **Steps**:
   1. Navigate to the Azure portal.
   2. Go to "Create a resource" and search for "Application Gateway".
   3. Select "Create" to begin the setup.
   4. Configure the basic settings:
      - Subscription
      - Resource Group
      - Name
      - Region
   5. Configure the settings for the frontend IP:
      - Select either Public or Private.
      - If Public, configure a new or existing public IP address.
   6. Configure the backend pool:
      - Add backend targets (VMs, IP addresses, or FQDNs).
   7. Set up the routing rules:
      - Create a listener and associate it with the frontend IP configuration.
      - Create a backend HTTP setting.
      - Configure path-based or basic routing rules.
   8. Review and create the application gateway.

### B. Test the Azure Application Gateway

1. **Steps**:
   1. Obtain the public IP address or DNS name of the Application Gateway.
   2. Use a web browser or HTTP client to send requests to the Application Gateway.
   3. Verify that the traffic is being correctly routed to the backend targets.
   4. Check the health status of the backend pool to ensure all targets are healthy.
   5. Review the metrics and logs to verify the performance and behavior of the Application Gateway.

## Verification

- Ensure that the Application Gateway correctly routes traffic to the backend pool.
- Verify the health status of all backend targets.
- Check the logs and metrics for any anomalies or performance issues.

## Additional Information

- For a detailed step-by-step visual guide, refer to the [YouTube Tutorial on Azure Application Gateway](https://www.youtube.com/watch?v=B3O6bXu-NbM).
- Consult the Azure documentation for advanced configurations and troubleshooting tips.
