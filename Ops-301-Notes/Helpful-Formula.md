| Subnet Mask     | CIDR Notation | Total IP Addresses | Usable IP Range               | Network Address | Broadcast Address |
|-----------------|---------------|-------------------|-------------------------------|-----------------|-------------------|
| 255.255.255.0   | /24           | 256               | 192.168.1.1 to 192.168.1.254  | 192.168.1.0     | 192.168.1.255     |
| 255.255.255.128 | /25           | 128               | 192.168.1.1 to 192.168.1.126  | 192.168.1.0     | 192.168.1.127     |
| 255.255.255.192 | /26           | 64                | 192.168.1.1 to 192.168.1.62   | 192.168.1.0     | 192.168.1.63      |
| 255.255.255.224 | /27           | 32                | 192.168.1.1 to 192.168.1.30   | 192.168.1.0     | 192.168.1.31      |
| 255.255.255.240 | /28           | 16                | 192.168.1.1 to 192.168.1.14   | 192.168.1.0     | 192.168.1.15      |
| 255.255.255.248 | /29           | 8                 | 192.168.1.1 to 192.168.1.6    | 192.168.1.0     | 192.168.1.7       |
| 255.255.255.252 | /30           | 4                 | 192.168.1.1 to 192.168.1.2    | 192.168.1.0     | 192.168.1.3       |

Explanation:
- Subnet Mask: The subnet mask used to divide the IP address into network and host portions.
- CIDR Notation: The CIDR notation representing the subnet mask.
- Total IP Addresses: The total number of IP addresses available in the subnet.
- Usable IP Range: The range of usable IP addresses, excluding the network and broadcast addresses.
- Network Address: The network address of the subnet.
- Broadcast Address: The broadcast address of the subnet.

Patterns:
- The network address is always the first IP address in the subnet.
- The broadcast address is always the last IP address in the subnet.
- The usable IP range excludes the network and broadcast addresses, and it starts from the second IP address and ends at the second-to-last IP address in the subnet.
