# Reading 03
---
# Why is this relevant?
- The first article these notes refer to teaches us to understand the nature of and effectively read CIDR Notation, while the second regards the importance of subnetting/network segmentation and breaks down the practice into greater detail. These are both vital pieces of information, and go hand in hand with one another, as it is vital to understand how CIDR blocks and notation works to understand what you are doing when segmenting a network. Network segmentation is extremely important as it is one of the most scalable and easily customized means of securing a network in both corporate and home environments.
# CIDR Block Notation
## What is CIDR notation? a CIDR block?
- CIDR notation is a method of representing a CIDR block.
- A CIDR block is a fancy name for an IP range.
- article specifies: when creating a network, the aim is to make sure there are enough IP addresses for your use case, without exceeding too far past what is necessary.
## How many octets are found in an IPv4 address?
- four, hence the name IPv4. an octet is an 8 bit decimanl number separated by dots, think 127.0.0.1
## Setting binary aside and using the decimal system, what is the range of numbers found in an octet?
- an 8 bit number represented in the decimal system has a range of 0-255. All four octets together add up to 32 bits, for a range of 0.0.0.0-255.255.255.255. In CIDR notation, this range is represented as 0.0.0.0/0.
## What does the final digit after the “/” represent in an IPv4 address?
- the final digit after the / represents how many bits make up the mask.
- bits that are masked do not change. The article cites the example 10.0.0.0/16. The 16 indicates half the available bits are being used for the mask. It will always move from first to last, left to right. 32/2 = 16. therefore half of the available 32 bits in this example are being used by the mask, and the range would be 10.0.0.0-10.0.255.255. if the CIDR block in the example were switched to 10.0.0.0/8, the range would be 10.0.0.0-10.255.255.255 and so on.
## How many IP addresses are in the CIDR block 10.0.0.0/24?
- this CIDR block would have 256 IP addresses, with a range of 10.0.0.0-10.0.0.255. this is calculated by calculating 2 to the power of the number of bits NOT being used by the subnet mask. 32 - 24 = 8, 2 to the power of 8 is 256. therefore there are 256 IP addresses in this CIDR block.
# Network Segmentation
## In your own words, describe network segmentation.
- Network segmentation is a broader term that encompasses both physical and logical segmentation. Physical segmentation takes place in the first layer of the OSI model, as networks are literally physically divided into subnets by physical devices such as routers, switches and cables. Logical segmentation occurs in layer 3 of the OSI model, and takes place when a network is further divided through software, such as a VPN. Network segmentation is simply a term for describing the division of a network.
## Network segmentation isn’t important as long as the network is using a well configured firewall. Do you agree? Why or why not?
- I strongly disagree. I would never ever argue against added layers of security, just to be safe. If you can get away with having a well segmented network without sacrificing performance, I say go for it. The firewall is definitely important, but segmenting your network can help to further improve your security through isolation and by ascribing specialized access control to certain subnets. Having physical layers to your network means more authentication is needed to move through it, and makes traversing from one layer to the next more difficult for would-be attackers. In a company setting, specialized access control can reduce the likelihood of attacks from within, or even just simple user errors on the part of lower level staff. Isolation keeps things in quarantine, which is why I use a subnet at home: whatever malware or weird changes to the network my roommates use won't affect me, and anything I do won't spread to every other device in the house. While a firewall is useful, it is only one part of a bigger picture; like having a liver without the kidneys.
## What is a screened subnet?
- subnets that expose externally facing systems. These operate on layers 3 and 4 of the OSI model, operating where the TCP handshakes and other protocols take place, and examining IP packets to determine what should be allowed through. Internet accessible resources are generally a good example, as they would filter out access to internal, backend data while still providing the user access to what they need.
## Cameras, ID card scanners, locked doors and biometrics are just a few examples of what type of security?
- Traditional Physical security! Any of these devices that are IoT Devices need to be on their own subnet, as they generally do not have the same levels of security that more advanced devices like laptops and smartphones do. (think ring doorbell hacks, unguarded wifi cameras being logged on websites for the public to watch, washington DC CC camera hack, etc.)
---
# Things I want to know more about
- How can a compromised industrial control system be dangerous to a corporate network?
- How do IT workstations prevent unauthorized access, as it seems these would be a vulnerable point through which the entire network could be compromised? What extra security measures need to be implemented here, and what does a typical network topology for IT workstations generally look like?
- Is creating a subnet the only way to secure physical security devices?