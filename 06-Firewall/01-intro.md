# Azure Firewall

- Filter traffic between cloud resources
- Example: VM1 in spoke 1 can communicate with VM's from Spoke 2
- Filter outbound traffic to the internet. Protects against data exfiltration
  Example: All spoke 1 VMs could not connect to internet, except some required API endpoints
- Filter traffic to/from on premises networks
- source and destination network adress translation (SNAT and DNAT) support
  Example: All outbound traffic will use Firewall public IP addresses
- By default, all traffic is denied
  <img width="584" height="582" alt="image" src="https://github.com/user-attachments/assets/9de028d1-b6b6-456a-b9fb-c698810e6466" />

## Creating Firewall

<img width="559" height="538" alt="image" src="https://github.com/user-attachments/assets/929bc48e-8403-441f-8fb2-3cb17767e27d" />


<img width="686" height="702" alt="image" src="https://github.com/user-attachments/assets/aa853aed-8a6b-404a-a8e4-2c36378df95d" />


## Azure Firewall Policy application rules

Filter on layer 7 (FQDN). all traffic is denied by default

Example: Allow access to www.microsoft.com

<img width="1283" height="420" alt="image" src="https://github.com/user-attachments/assets/e80c6c61-c612-4f95-8c3a-3cdb17deafce" />

## architecture

<img width="1163" height="509" alt="image" src="https://github.com/user-attachments/assets/24f454a1-9a27-4ce8-a809-5ad0fe931797" />

## Azure Firewall Policy Network rules

- Filter on Layer 3 - 4 (IP addresses, Port number, Protocol), like NSG's
- Example Allow communication between spokes

<img width="879" height="342" alt="image" src="https://github.com/user-attachments/assets/b45a7950-38a0-4f2a-8453-efd997866b0d" />

<img width="916" height="497" alt="image" src="https://github.com/user-attachments/assets/d4563546-7b48-429e-a141-1d0f0c2facc0" />





<img width="594" height="509" alt="image" src="https://github.com/user-attachments/assets/a4d7e86a-e608-4da5-92a8-58bf269e0797" />




