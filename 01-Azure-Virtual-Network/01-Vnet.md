# Azure Virtual Networks - VNET

## introduction
- VNET is private network in Azure
- Azure services like VM's are always attached to a VNET
- Resources within the same VNET could securely communicate with
  - each other
  - The internet
  - on-premises networks
- VNET is similar to a tradional network that you'd operate in your own datacenter.
- Range of private IP addresses to be used by Azure services. For example: 10.0.0.0/8

## Features
- communication of Azure resources with the internet
  Public IP, Load Balancer, NAT Gateway
- Communication between Azure resources
  By default, resource within the same VNET can communicate with each other
- Communication between multiple VNET's
  VNET peering in hub and spoke
- Communication with on-premises resources
  Express Route, S2S VPN
- Filtering of network traffic through NSG or NVA Firewall
- Routing of network traffic through Route Table
- Integration with Azure services through Private Endpoint

## Virtaul Network - Subnet


- Segments the virtual network into one or more subnetworks
- Allocate the portion of the VNET address space into each subnet
- you can then deploy Azure resources in a specific subnet
- subnet can help improve security by using NSG's to control traffic between subnets

## Virtual Network Address Space

RFC 1918

- 10.0.0.0 - 10.255.255.255 (10/8 prefix)
- 172.16.0.0 - 172.31.255.255 (172.16/12 prefix)
- 192.168.0.0 - 192.168.255.255 (192.168/16 prefix)

<img width="1488" height="757" alt="image" src="https://github.com/user-attachments/assets/cfbf445d-df68-4708-8c50-02c94f250918" />


## creating VNET with Azure cli and terraform
```
az network vnet create -g rg-demo-vnet -n vnet-demo --address-prefixes ["10.0.0.0/16"]
az network vnet subnet create -g rg-demo-vnet --vnet-name vnet-demo -n subnet-frontend--address-prefixes ["10.0.0.0/24"]
```

-------
```
resource "azurerm_virtual_network" "vnet" {
  name                = "vnet-spoke"
  resource_group_name = azurerm_resource_group.rg.name
  location            = azurerm_resource_group.rg.location
  address_space       = ["10.0.0.0/16"]
}
resource "azurerm_subnet" "subnet-frontend-servers" {
  name                   = "subnet-frontend-servers"
  resource_group_name    = azurerm_virtual_network.vnet.resource_group_name      
  virtual_network_name   = azurerm_virtual_network.vnet.name        
  address_prefixes       = ["10.0.0.0/24"]
  private_endpoint_network_policies_enabled = false
}

```

## Creating VNET in portal

<img width="1058" height="670" alt="image" src="https://github.com/user-attachments/assets/e2b3c357-d981-4b08-9573-ec7f3a6940a7" />

-----
<img width="1262" height="707" alt="image" src="https://github.com/user-attachments/assets/daafa874-f1e0-4016-80a4-6f17842a7be3" />

-----
<img width="865" height="679" alt="image" src="https://github.com/user-attachments/assets/194474ef-8c0a-4ec4-9573-b4380119455c" />
-----
<img width="1246" height="671" alt="image" src="https://github.com/user-attachments/assets/6340b8fe-60dd-428d-a01a-5621a5ce175c" />

-----
<img width="527" height="691" alt="image" src="https://github.com/user-attachments/assets/0b73860a-c124-4e0e-a037-4a18855a75b4" />






