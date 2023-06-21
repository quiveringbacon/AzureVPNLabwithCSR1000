# Azure VPN Lab with CSR1000

This creates an onprem vnet with Cisco CSR1000v connected to a hub vnet vpn gateway and a spoke vnet attached to the hub. VM's are created in all 3 vnets. You'll be prompted for the resource group name, location where you want the resources created, your public ip, and username and password to use for the VM's and NVA. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs. The topology will look something like this:

![image](https://github.com/quiveringbacon/AzureVPNLabwithCSR1000/assets/128983862/b05f05b3-9719-447a-bcf3-96d066233889)


You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone  https://github.com/quiveringbacon/AzureVPNLabwithCSR1000.git ./terraform".
Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.

