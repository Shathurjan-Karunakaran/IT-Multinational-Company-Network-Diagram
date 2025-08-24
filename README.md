# Multinational IT Company Network Design

## Project Overview
This project presents a comprehensive network design for a multinational IT company establishing a new overseas branch in Sri Lanka. The design implements a secure, organized, and optimized network infrastructure for a three-story building using Cisco Packet Tracer.

## Building Specifications
- **Structure:** 3-story building (Ground, First, Second floors)
- **Dimensions:** 60m × 30m × 12m (4m per floor)
- **Available IP Range:** 10.10.0.0/16

## Network Architecture

### Department Distribution
The network serves 5 main departments across 3 floors:

#### Management Office (Ground Floor)
- CEO Room: 2 devices
- Staff Room: 2 devices
- Board Room: 3 devices
- Printing Room: 2 devices
- Lobby Area: 1 device

#### Admin Department (Ground Floor)
- Finance Section: 15 devices
- Human Resource Section: 25 devices
- Assistant Section: 10 devices
- Printing Room: 2 devices

#### Technology Department (First Floor)
- R&D Section: 25 devices
- Design Section: 125 devices
- Test Section: 20 devices
- Meeting Room: 3 devices

#### Operations Department (First Floor)
- Branding Section: 8 devices
- Reporting Section: 10 devices
- Sales Section: 40 devices

#### Marketing Department (Second Floor)
- Marketing Strategies Section: 5 devices
- Public Relations Section: 10 devices

## VLAN Design & IP Allocation

| VLAN ID | Department/Section | Required IPs | Allocated Size | IP Range | Subnet Mask | Gateway |
|---------|-------------------|--------------|----------------|-----------|-------------|---------|
| 10 | Management Office | 10 | 14 | 10.10.1.81-10.10.1.94 | /28 | 10.10.1.81 |
| 20 | Lobby Area | 1 | 2 | 10.10.1.105-10.10.1.106 | /30 | 10.10.1.105 |
| 30 | Operations Dept | 58 | 62 | 10.10.0.129-10.10.0.190 | /26 | 10.10.0.129 |
| 40 | Admin Department | 52 | 62 | 10.10.0.193-10.10.0.254 | /26 | 10.10.0.193 |
| 50 | Technology Dept (Design) | 125 | 126 | 10.10.0.1-10.10.0.126 | /25 | 10.10.0.1 |
| 60 | Technology Dept (R&D/Test) | 48 | 62 | 10.10.1.1-10.10.1.62 | /26 | 10.10.1.1 |
| 70 | Marketing Strategies | 5 | 6 | 10.10.1.97-10.10.1.102 | /29 | 10.10.1.97 |
| 80 | Public Relations | 10 | 14 | 10.10.1.65-10.10.1.78 | /28 | 10.10.1.65 |

## Key Features

### Security Implementation
- **VLAN Segmentation:** Each department isolated in separate VLANs
- **Access Control:** Restricted printer access within departments
- **Password Protection:** Individual node passwords for administrator access
- **Lobby Isolation:** Separate VLAN for guest access
- **Management Privileges:** Special access rights for management to admin department

### Network Optimization
- **Efficient IP Allocation:** Variable Length Subnet Masking (VLSM) implementation
- **Department Segregation:** Technology and Marketing departments split into multiple VLANs
- **Scalable Design:** Room for future expansion

### Equipment Configuration
- **Main Router:** Cisco ISR4331 with enhanced security features
- **Core Switch:** Cisco 3640-24PS multilayer switch
- **Wireless Coverage:** Home routers with static IP allocation
- **Redundancy:** Dual power supply configuration

## Files Included
- `network_design.pkt` - Complete Cisco Packet Tracer file
- `README.md` - This documentation file

## Network Topology
The network follows a hierarchical design:
1. **Core Layer:** Main router (ISR4331) providing internet connectivity
2. **Distribution Layer:** Multilayer switch (3640-24PS) handling VLAN routing
3. **Access Layer:** Department switches and wireless access points

## Testing & Verification
- Inter-VLAN communication configured and tested
- Printer access restrictions verified
- Security policies implemented and validated
- Network performance optimized for all departments

## Requirements Met
✅ Optimized IP address utilization using VLSM  
✅ Department-specific network segmentation  
✅ Secure access control implementation  
✅ Scalable network design  
✅ Professional documentation and diagrams  

## How to Use
1. Open the `.pkt` file in Cisco Packet Tracer
2. Review the network topology and configurations
3. Test connectivity between different VLANs
4. Examine security implementations
5. Refer to the PDF for detailed configuration steps

## Future Enhancements
- Implementation of additional multilayer switches for high-traffic scenarios
- Advanced security features (firewalls, intrusion detection)
- Network monitoring and management tools
- Disaster recovery and backup solutions

## Contact
For questions or collaboration opportunities, please reach out through the repository issues or discussions.

---
*This project demonstrates practical network design skills using industry-standard tools and best practices for enterprise network implementation.*
