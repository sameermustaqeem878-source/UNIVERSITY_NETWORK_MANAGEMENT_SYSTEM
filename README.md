
# University Network Management System

A three-layer hierarchical campus network designed and simulated using Cisco Packet Tracer. The project demonstrates how a university network can be organized through VLAN segmentation, centralized DHCP, dynamic routing, access control lists, and wired and wireless connectivity.

## Project Overview

The network is designed to connect different university departments while maintaining controlled communication between them.

It follows a hierarchical network architecture consisting of:

- Core Layer
- Distribution Layer
- Access Layer

Each department operates in a separate VLAN and subnet. Routing, IP allocation, and security policies are configured to manage communication across the campus network.


## Network Architecture

The campus network follows a three-layer hierarchical design.

### 1. Core Layer

- Provides the central network backbone.
- Uses a multilayer switch for core connectivity.
- Includes the centralized DHCP server.
- Uses VLAN 99 for core network management.

### 2. Distribution Layer

- Connects the core network with departmental networks.
- Handles inter-VLAN and inter-departmental routing.
- Uses OSPF for dynamic routing.
- Applies ACLs to control network traffic.
- Uses VLAN 100 for distribution links.

### 3. Access Layer

- Connects end-user devices to the network.
- Includes departmental switches, desktop PCs, and wireless access points.
- Provides wired and wireless connectivity across campus departments.

## VLAN and IP Addressing Scheme

| Department / Zone | VLAN ID | Subnet | Purpose |
|---|---:|---|---|
| Core Network | 99 | `192.168.99.0/24` | Core management and DHCP server |
| Admin Block | 10 | `192.168.10.0/24` | Administration and management |
| Academic Block | 20 | `192.168.20.0/24` | Classrooms, labs, and faculty |
| Library | 30 | `192.168.30.0/24` | Research and library resources |
| Hostel | 40 | `192.168.40.0/24` | Residential student network |
| IT Department | 50 | `192.168.50.0/24` | Technical support and monitoring |
| Distribution Links | 100 | — | Inter-router and distribution connections |

## Key Features

### Centralized DHCP

- Uses a centralized DHCP server for automatic IP address allocation.
- Configures `ip helper-address` on departmental router sub-interfaces.
- Reduces manual IP configuration and address assignment errors.

### VLAN Segmentation

- Separates university departments into individual VLANs.
- Assigns a dedicated subnet to each department.
- Helps organize network traffic and restrict unnecessary communication.

### Dynamic Routing with OSPF

- Uses OSPF in Area 0.
- Allows routers to exchange routing information dynamically.
- Calculates routes between network segments.
- Supports alternate routing paths when network links become unavailable, provided an alternative path exists.

### Access Control Lists (ACLs)

Network access is controlled through configured ACL policies.

| Access Policy | Description |
|---|---|
| Admin Full Access | Admin VLAN 10 can access all campus subnets. |
| Library and Hostel Access | VLAN 30 and VLAN 40 are allowed to communicate with each other. |
| Department Isolation | Other unauthorized cross-department communication is blocked. |

### Wired and Wireless Connectivity

- Provides wired connections for desktop computers.
- Uses wireless access points for wireless devices.
- Supports connectivity across the university departments.

## Technologies and Tools

| Technology | Purpose |
|---|---|
| Cisco Packet Tracer | Network design and simulation |
| VLAN | Network segmentation |
| DHCP | Automatic IP allocation |
| OSPF | Dynamic routing |
| ACL | Network access control |
| Cisco IOS CLI | Device configuration |
| Ethernet | Wired connectivity |
| Wireless Access Points | Wireless connectivity |

## Network Testing

The following tests can be performed in Cisco Packet Tracer to verify the network configuration:

1. **DHCP Testing:** Verify that devices receive IP addresses automatically.
2. **Connectivity Testing:** Use `ping` to test communication between permitted network segments.
3. **VLAN Testing:** Confirm that devices are assigned to their correct VLANs.
4. **ACL Testing:** Verify that permitted traffic is allowed and unauthorized communication is blocked.
5. **OSPF Testing:** Check routing tables and OSPF neighbor relationships.
6. **Fault Tolerance Testing:** Disconnect a network link and verify whether OSPF selects an available alternative path.

## Getting Started

### Requirements

- Cisco Packet Tracer installed on your computer.
- The project `.pkt` file from this repository.

### Run the Project

1. Download or clone this repository.
2. Open Cisco Packet Tracer.
3. Open the `.pkt` project file.
4. Inspect the network topology and connected devices.
5. Select any router or switch to access its CLI.
6. Use the following command to enter privileged EXEC mode:

```bash
enable
```

7. Test DHCP, routing, VLAN communication, and ACL policies.
8. Use Simulation Mode to observe how packets travel through the network.

## Learning Outcomes

Through this project, we practiced:

- Designing a hierarchical campus network.
- Configuring VLANs and subnet addressing.
- Implementing centralized DHCP services.
- Configuring OSPF dynamic routing.
- Applying ACL-based network security.
- Connecting wired and wireless devices.
- Testing network connectivity and routing behavior.
- Understanding network segmentation and fault tolerance.

## Author

**Muhammad Sameer**

- GitHub: [sameermustaqeem878-source](https://github.com/sameermustaqeem878-source)
- LinkedIn: [Muhammad Sameer Mustaqeem](https://www.linkedin.com/in/m-sameer-mustaqeem-b1a436317/)

---

**Project:** University Network Management System  
**Institution:** Air University  
**Department:** Software Engineering
