# Secure Small Office Network & Troubleshooting Lab

## About the Project

I built this network using Cisco Packet Tracer to practice configuring and securing a small office network.

The network has three departments: IT, HR, and Guest. Each department is assigned to a separate VLAN to keep its traffic organized and control communication between departments.

## Network Devices

- 1 Cisco 2911 Router (R1)
- 2 Cisco 2960 Switches (SW1 and SW2)
- 6 PCs across the three departments


## VLANs and IP Addressing

- **IT (VLAN 10)**
  - Network: 192.168.10.0/24
  - Default Gateway: 192.168.10.1

- **HR (VLAN 20)**
  - Network: 192.168.20.0/24
  - Default Gateway: 192.168.20.1

- **Guest (VLAN 30)**
  - Network: 192.168.30.0/24
  - Default Gateway: 192.168.30.1

## Configurations

- Created VLANs for IT, HR, and Guest.
- Configured trunk links between the switches and the router.
- Set up inter-VLAN routing using Router-on-a-Stick.
- Configured DHCP pools to assign IP addresses automatically.
- Applied an ACL to prevent Guest devices from accessing the IT and HR networks.
- Enabled Port Security on user-facing switch ports using sticky MAC addresses.

## Testing

I tested the network to check that:

- Devices received IP addresses through DHCP.
- Devices in different VLANs could communicate through the router where permitted.
- Guest devices were restricted from accessing the IT and HR networks.
- Port Security was configured on the access ports.

## Project Files

- `Packet-Tracer/` – Contains the Packet Tracer project file.
- `Screenshots/` – Contains screenshots of the topology, VLANs, trunk links, DHCP, security configurations, and connectivity tests.

## Tools

- Cisco Packet Tracer
- Cisco IOS CLI
