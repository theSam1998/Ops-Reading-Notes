# Reading 04
---
## Relevancy statement:
- this reading discusses how the networking settings in virtualbox work, and how they can be used to create virtual systems that function better for our intended purposes. This is crucial to our learning in this unit, as not only do we use virtualbox extensively, but we also are working on developing a solid understanding of networking, and through the use of these settings we can simulate all kinds of different networks in virtual box.
## Which network mode in VirtualBox can be used to emulate unplugging the Ethernet cable from the network?
- Not Attached is the network setting that will allow you to simulate unplugging the ethernet cable. This can be extremely useful for network troubleshooting, as it makes it easier to determine whether the issue is client-side or sever-side.
## Which network mode would be best if you wanted to run a server on a VM that could be fully accessible from your physical local area network?
- Bridged! this is the one I use for my home server vm, a bridged network connects the vm to the host network interface, meaning it directly connects through your host machine to the internet rather than routing through another connection. The default gateway will be the same as the host machine's, and the host machine must be connected to the internet for bridged mode to work (some other kinds of vms can connect to the internet independently of the host machine, such as NAT)
## What are the three options of promiscuous mode and what does each do?
- promiscuous mode is a setting available for bridged, nat network, internal network, or host only adapter. This mode allows the virtual network adapter to pass all traffic, regardless of which adapter the traffic is set to go through. This mode can be useful for troubleshooting, as it gives you greater visibility of network traffic. There are three settings available for promiscuous mode, as follows:
- deny: any traffic not addressed to the vm's virtual network adapter is denied entry
- allow vms: allows only traffic transmitting to and from virtual machines.
- allow all: allows all network traffic to pass through the virtual network adapter.
## What is Port Forwarding?
- port forwarding is another useful setting in virtual box. Port forwarding enables you to direct traffic from one port to the same port on another device. In virtual box, this setting allows you to divert traffic from ports on your physical machine to your virtual machine. This can be useful for remotely accessing a virtual web server, or similar functions. 
---
## Things I want to know more about
- how does port forwarding work
- how does adding in vms to a network complicate the network topology? Does this bring the same risks as adding new physical devices? Is it more or less risky?
- what is the most scalable set of network settings for a virtual machine (i.e. what settings would you use if you may need to add new vms to the network at any moment, and there is a large volume of vms providing traffic on the network?