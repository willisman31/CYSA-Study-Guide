# Virtualization

## Explanation

Virtualization is a mechanism for abstracting hardware into code; this means that a single physical server can actually host many different systems on top of it.  This creates a cost benefit, because separate hardware is no longer a requirement for running separate systems.  These separate systems have limited visibility into each other (if they have any at all) and they are run by a "hypervisor".  The hypervisor manages these systems at a high level and allocates hardware resources as configured by the administrator.  

## Importance

Virtualization provides security benefits because different systems can exist on the same hardware so that if one application running on one system is compromised, the others maintain an additional layer of security.

## Example

VirtualBox is a hypervisor that can be run on top of Windows or MacOS; it allows you to run a separate operating system on top of your existing system.  VMWare, Hyper-V, and OpenShift are also hypervisors that accomplish virtualization to similar effect.

## Resources

- [VMWare - What is virtual infrastructure?](https://www.vmware.com/topics/glossary/content/virtual-infrastructure.html)
- [DNSStuff - What is Virtual Infrastructure and How to Manage It](https://www.dnsstuff.com/what-is-virtual-infrastructure)
- [IBM - Virtualization](https://www.ibm.com/cloud/learn/virtualization-a-complete-guide)