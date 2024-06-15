# Task-5 : Domain and DNS Server Setup

## Resources

- [YouTube Tutorial on Setting Up a Domain and DNS Server](https://www.youtube.com/watch?v)

## Tasks

### A. Set Up a Domain

1. **Steps**:
   1. Purchase a domain from a domain registrar (e.g., GoDaddy, Namecheap).
   2. Log in to the domain registrar's control panel.
   3. Find the DNS management section for your domain.
   4. Note the nameservers provided by the registrar.

### B. Set Up a Server on a VM

1. **Steps**:
   1. Navigate to the Azure portal.
   2. Go to "Create a resource" and select "Virtual Machine".
   3. Configure the VM settings:
      - Subscription
      - Resource Group
      - VM Name
      - Region
      - Image (e.g., Ubuntu Server or Windows Server)
      - Size
   4. Configure the administrator account:
      - Username
      - Authentication type (password or SSH public key)
   5. Configure networking settings:
      - Virtual Network
      - Subnet
      - Public IP address
   6. Review and create the VM.
   7. Once the VM is created, connect to it using SSH (Linux) or RDP (Windows).
   8. Set up your server application (e.g., web server like Apache or Nginx).

### C. Use the DNS Server for Traffic

1. **Steps**:
   1. In the domain registrar's DNS management section, create DNS records to point your domain to your VM's public IP address.
      - **A Record**: Maps your domain to the public IP address of your VM.
      - **CNAME Record**: Maps subdomains to your domain.
   2. Save the DNS settings and wait for them to propagate (this may take some time).
   3. Verify the DNS setup by using a tool like `nslookup` or `dig` to check the DNS records.
   4. Ensure that accessing your domain in a web browser directs traffic to your VM's server.

## Verification

- Ensure the domain points to the correct IP address of your VM.
- Verify that the server on the VM is accessible via the domain name.
- Test the DNS propagation using tools like `nslookup` or `dig`.
- Confirm that the web server or application on the VM responds correctly when accessed through the domain.

## Additional Information

- For a detailed step-by-step visual guide, refer to the [YouTube Tutorial on Setting Up a Domain and DNS Server](https://www.youtube.com/watch?v).
- Consult the Azure and domain registrar documentation for advanced configurations and troubleshooting tips.
