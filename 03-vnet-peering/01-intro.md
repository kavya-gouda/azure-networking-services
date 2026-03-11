# Virtual Network peering

- Connect two or more VNET's
- Enables resources within peered VNET's to communicate with each other privately
- Traffic between VM's in peered VNET's uses Microsoft backbone infrastructure
- A VNET could be peered to one or more VNETS
- Address ranges should not overlap
- Peering is not transitive
- VNET 2 and 4 cannot communicate directly, could be done via NVA and IP Forwarding
- Peered VNET's could be in different Azure regions This is Global peering

<img width="537" height="655" alt="image" src="https://github.com/user-attachments/assets/d17f608f-d87f-426b-9248-ad241b0d7669" />

## VNET peering and topologies
- Hub and spoke
- Mesh
- Hub and Spoke with direct connectivity between spokes

<img width="1185" height="565" alt="image" src="https://github.com/user-attachments/assets/d9f4d2f2-cac9-4cb6-b38e-ab3c0188de9a" />

## Gateway and connectivity with on-premise networks

- To connect on-premises networks, you can use Gateway
- Gateway could be used also for network connectivity

<img width="713" height="394" alt="image" src="https://github.com/user-attachments/assets/dc309b73-6969-45c4-a5ef-c98154eed3d4" />

## Creating VNET peering

<img width="640" height="252" alt="image" src="https://github.com/user-attachments/assets/cde15767-0aa8-4576-b220-f41f738e4b31" />

<img width="547" height="710" alt="image" src="https://github.com/user-attachments/assets/05add970-8f8f-4e6d-a4c8-259470a6a577" />

- 
