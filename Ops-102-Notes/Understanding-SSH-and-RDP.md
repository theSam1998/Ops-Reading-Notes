# Understanding SSH and RDP
---
## SSH Protocol
### What is the Secure Shell (SSH) Protocol?
- The SSH protocol is a method of logging in from one computer to another securely using the terminal and a network connection between the two devices. It allows for all the control that the terminal of that device would, without ever having to touch the device in question.
### What are the typical uses of the SSH protocol?
- providing secure access for users and automated protocols. This is done through the encryption and authentication of information transferred between the two devices. So, for example, when operating in the SSH protocol, I had to know not only the IP, but the username and password of the device I wanted to connect to. SSH authenticating this information is the only reason this would work to allow me to connect. Other programs, like WinSCP, rely on SSH to accomplish secure file transfers and other desired tasks. SSH can also be used to issue commands to the connected device through the console, which makes it useful for network admins who may need to quickly and remotely access a device or group of devices to issue commands/update files/otherwise provide services. This makes it useful for network infrastructure as well.
### How does the SSH protocol work?
- It begins with the client (the device you intend to connect to) establishing a connection with the server (the device you are accessing SSH from). From here, the server will send a public server key (a large, multi-digit key used to encrypt information shared between the two devices) to the client, which is then verified by the client. From there, a secure channel is opened via this key. The user will be prompted to log into the host OS, and from this point data can now be successfully and securely shared between the two devices.
### How is the data kept safe when transmitted between the SSH client and server?
- The data passes through multiple levels of encryption. There are two keys in the method we use most often with SSH, a public key and a private key. the public key is used to authorize access to anybody who possesses the private key, after both are configured. this type of encryption is known as "symmetrical encryption".
note - key pairs created by the user are only used for authentication, not encryption. The key that will be used for encryption by both devices is designed during the initial negotiation between the SSH server and client.
### What is SFTP?
- Secure File Transfer Protocol, it is a method of transferring files from one device to another using the SSH protocol. It relies on the encryption process of SSH to securely transfer information without providing opportunities for compromise.
## RDP
### What is Windows Remote Desktop Connection?
- RDC is another method of accessing and manipulating a device remotely. Unlike SSH, RDP does have a GUI, and displays the GUI of the system being accessed. RDC does offer a secure connection, although it uses a different method of encryption from SSH, relying on the RC4 cipher to encrypt data, which is something I am not familiar with yet. Noted in my googling, RC4 is designed for efficient encryption of small amounts of data and can use a 56 or 128 bit key. I will need to research this more to properly grasp the terms that are being used here.
### What is RDP?
- RDP is the protocol the RDC application relies on to work.
### What is the RDP port number?
- 3389

## Things I want to know more about
- I want to understand more about the different types of encryption and ciphers that are out there, there was a lot of terminology in the side research I had to do to answer these questions that I had a hard time understanding.
- Which method of remote connection is preferred by who and why? RDP or SSH?
- What are the most common uses of these programs in the security field?
- How can I understand these programs better to work with them more efficiently
