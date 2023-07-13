# Active Directory and Its Key Services
---
## Statement of relevance:
- Microsoft Active Directory service is a commonly used tool in the industry for managing large groups of users, such as in a corpoprate network. It is made up of several directory services, which are a type of database used for storing information about users and resources. Being commonly used in the field for a variety of purposes surrounding AAA and management of groups, it is vital for us to familiarize ourselves with how it works and not only how it can be used, but what its vulnerabilities are and how they can be exploited so we can better understand how to keep our systems secure. 
## What exactly is “Active Directory” and are the key services it provides?
- Active Directory is an identity management service made for windows domain networks. it is composed of several different directory services, such as AD CS(active directory certificate services), which issues and manages digital certificates (a password or file that proves the authenticity of a device, server, or user per fortinet. It is used to ensure that only trusted users and devices can access network resources. It is also commonly used for HTTPS: the secure sockets layer (SSL) certificate is a form of digital certificate.). Another example is AD RMS (active directory rights management services), which manages access permissions to files and other resources. 
- Its key features include: 
- providing a schema, which defines the classes (classes adefine the set of mandatory and optional attributes an object can have) of objects and attributes in the directory (user accounts and other things ranging from applications and shared folders to printers and PCs, attributes are a set of fields that define what additional data can be attributed to the object, per windows-active-directory.com). All this talk of objects leads me to think AD DS would be quite friendly to python.
- providing a global catalogue, which contains detailed information about every object in the directory
- providing a query and index mechanism, which allows hosts to efficiently find directory information. 
- providing a replication service, to spread the data across the network.
## What are the differences between a domain, forest, and tree in Active Directory?
- A domain is a collection of objects that share the same active directory. a domain is identified by a dns name, like yourgroup.com
- a tree is a collection of domains with a common, consistent dns root name (think back to the previous lab. admin.globexpower.com was a tree in the forest, that's not a metaphor, it's literally the terminology for what is technically going on with this system. admin was the branch, with the root name of globexpower.com).
- a forest is a collection of trees that have a common schema, global catalogue and directory configuration, but not a common rootname. The forest is typically the security boundary for the network, essentially the bubble that contains the contents of the directory as a whole.
## How can objects (e.g. users, devices) within a domain be grouped?
- objects within a domain are grouped into organizational groups to make administration and management easier for large numbers of users at once. Admins can make organizational units to monitor just about anything, and apply group policies to them accordingly to make administration more efficient. These units also make it easier to delegate control and access to resources among other administrators at different levels.
## Explain the benefits of Active Directory, as you would to a family member.
- Without active directory, You would have to go from office to office, building to building, and potentially city to city or country to country to perform the amount of system configurations that would need to be done to manage the scale of users that exist in many businesses today. Active directory provides a framework that operates across the entire network to make it so you can configure entire groups of staff's devices in one go, allowing you to perform adminstrative tasks efficiently and focus your time on more important things that need to be done.
---
## Things I want to know more about:
- What are some things python can do with AD DS that powershell cannot?
- What are some of the best things to automate/write scripts for in AD DS?
- What are AD DS's weak points? Where do its biggest vulnerabilities lie and how can they be exploited?
