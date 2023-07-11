# Reading 06
---
## Statement of relevance:
- These materials are meant to familiarize us with NAT (Network Address Translation) and how it works. NAT is a vital part of establishing a proper, complete network with fully functional internet access, as this is the process by which the urls we are familiar with (i.e. https://www.google.com) are translated into their respective IP addresses, and vice versa. NAT also serves to translate and mask ports, serving in two ways to help direct traffic to its intended destination. Therefore, understanding how it works and how to use it properly to a T is vital to our future as cybersecurity professionals.


### 🤖 ChatGPT Correction:
- NAT's primary role is to allow multiple devices in a local network to share a single public IP address for internet access. This is achieved by translating the private (local) IP addresses of the devices into a public IP address and vice versa. The router keeps track of these translations and ensures that data coming from the internet is correctly directed to the device that requested it.

## What is the main purpose for implementing NAT on a network?
- As I mentioned earlier, NAT is simply the process by which URLs are translated into their respective IP addresses. This process occurs within the router, and translated information is sent from the router to both the internet and other devices on the network. Similarly, information to be translated is sent to the router from both the internet and other devices on the network. This process leads to ease of use for all users, as either valid IPs or URLs can be accepted by web browsers, software applications, and even shell commands or scripts you are writing. Without NAT, to access websites on a web browser, you would need to know the exact IP of every website you wanted to visit in order to do so. This translation process works because NAT translates local IP addresses into global IP addresses, and vice versa. therefore, NAT's main purpose is to help the traffic be directed to its intended destination, as without it IP address conflicts could occur (the article cites an example of a host trying to transmit information to another host, and because NAT is not working on one or more of the hosts, the other host tries to reply with the intended information to the wrong IP address, and the connection is incomplete.).

## At what layer of the OSI model does NAT happen?
- NAT is a tricky one. It is technically a network (3) protocol, but it also requires transport (4) to function properly. It modifies the IP address information in the header of each packet as it passes through the router, but also translates the port numbers used by transport layer protocols like TCP and UDP.

## What happens to packets when NAT runs out of addresses in the pool of available IPs?
- I am going to directly quote the geeksforgeeks article here as I feel it sums it up just fine. "If NAT runs out of addresses... then the packets will be dropped and an ICMP host unreachable packet is sent to the destination."

## What disadvantage does using NAT pose for routers?
- One of the disadvantages of NAT is that the process takes extra time. This results in switching path delays, which are exactly what they sound like: delays caused by the time it takes for the translation and path switching process to occur. This is typically not a problem on small, simple networks, but on complex networks that utilize multiple routers, switches, both or more, these delays can add up to become a significant problem. However, there are solid ways to counteract this issue that do not take too much time or maintenance.
- Certain applications may not function properly with NAT enabled on your network. These are primarily applications that utilize VoIP, online gaming applications, and other things that directly involve transmitting large amounts of data that need to be sent to specific detinations, like video conferencing and filesharing apps. NAT can cause interferences with the media traffic and signaling used to transmit this data by these applications, resulting in packet loss, lag and high latency.
- NAT can complicate tunneling protocols such as IPsec. This is because it changes the IP addresses in the headers of each packet, which directly interferes with the encryption and authentication process used by IPsec. IPsec relies on the original IP address of the corresponding device to ensure the data is being transmitted from the correct location. When NAT changes the IP address header, this can cause this authentication process to be broken, resulting in a loss of connection.
- causes the router to meddle into layer 4, as NAT directly interferes with the port numbers in the packet headers. Layer 4 functions are outside the intended scope of operations for routers, and this can lead to severe network instability as the router begins attempting to make modifications in a field it does not really understand, essentially.
---
## Things I want to know more about
- if NAT has so many problems, why is it so commonly used?
- is NAT really as commonly used as I believe it is?
- without NAT, how would a user be able to access the internet using URLs as opposed to simply the IPs of websites?
---
## 🤖 ChatGPT Additions:

### NAT Inside and Outside Addresses:
- NAT distinguishes between addresses that are in control of an organization (inside) and those that are not (outside). Inside addresses are those that need to be translated, while outside addresses are the network addresses where the translation is done.

### Types of NAT:
- NAT can be configured in three ways: Static NAT, Dynamic NAT, and Port Address Translation (PAT).
    - Static NAT: This provides a one-to-one mapping between local and global addresses. Mostly used for web hosting.
    - Dynamic NAT: Translates unregistered private IP addresses into registered public IP addresses from a pool. If the pool is exhausted, packets get dropped.
    - Port Address Translation (PAT): Also known as NAT overload, it allows multiple local IP addresses to be translated to a single public IP address using different port numbers. This is cost-effective and widely used.

### Advantages of NAT:
- NAT helps to conserve the number of legally registered IP addresses by allowing multiple devices to share a single public IP address.
- It provides privacy as the IP addresses of the devices in the local network are hidden from the outside world.
- It prevents the need for renumbering IP addresses when a network evolves.

** ChatGPT Signature **
---
### Model used 🤖
- ChatGPT4
### Prompt used ✍🏻
- [article text here] Scan the article above this command, as well as the notes I've taken on this article which lie below this command. Please analyze the information in both, and determine if there is anything in the article I have failed to implement into my notes that may be useful for future reference. If there is, please implement it into my notes by rephrasing it in a descriptive way that is consistent with the writing style I have used in my notes. Please also correct any incorrect information in the notes I have taken by rephrasing it into its correct form. Please keep the formatting in markdown consistent with the way I have formatted my notes, but I want you to add in some kind of indicator that any addition or change you make was made by you, whether this is a signature, a "chatgpt addition" header above the note, or whatever else you decide is best. please do not make any modifications to my notes unless the information in that particular place is incorrect. do not forget to add a signature, and format it in raw markdown, not rendered. the notes are here: [notes raw markdown here]
- prompt required 2 modifications to provide ideal output, final output required 2 modifications to integrate into notes properly.
- post output prompt: Please do not provide my original notes, only information from the article that you feel was not reflected in my notes, formatted in raw markdown. Please use your own words to phrase the information, elaborating further where needed.