# Azure Network Security Group (NSG)

<img width="410" height="605" alt="image" src="https://github.com/user-attachments/assets/c0b482e9-3d29-4c84-91e9-2b3ae1711ca0" />

<img width="899" height="474" alt="image" src="https://github.com/user-attachments/assets/88f49633-24af-440e-b667-28f756b9aebd" />

## What is the problem?

- By default, network traffic is allowed inside a virtual network(VNET) and from and to the internet
- all services can communicate with each other within a VNET
- This is not secure! Potential data exfiltration
- you should apply Zero-trust Network
- you should limit as much as possible the unnecessary traffic.

## What is Network Security Group - NSG?

- NSG filters Network traffic between Azure resources within the VNET.
- NSG uses security rules to allow or deny the inbound and outbound traffic for azure resources
- For each rules, it specifies the  source IP and destination IP Addresses, Port number and protoco

----
<img width="1294" height="770" alt="image" src="https://github.com/user-attachments/assets/5accbf6b-7531-431c-9a13-880d8a9fcfe6" />

