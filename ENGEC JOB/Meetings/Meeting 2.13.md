OSDI is a top-tier conference in systems that involves more systems (hardware and software) work. 

In order to pass IO to VMs, you need to have the device driver inside the Host OS and the VM, which introduces latency. PCIe passthrough allows a physical PCIe device to directly accessed by a VM. The PCIe configuration space involves 4 kB (the first 255 is for legacy PCI devices) which have many unassigned regions (linked list of devices with pointers to next device). Some capabilities are given to the device while some are not.

Unassigned PCI registers are exposed to the VM. There are some risks. There are two types of crashes:
1. **host crash**: writing malicious data to passthrough PCIe configuration space as a guest causes errors for the Host CPU
2. **device crash**: writing malicious data to passthrough PCIe configuration space as a guest breaks the device (power control etc.)

If vfio-pci hides something, then it leads to unassigned space for the guest, which actually leads to a lot of unwanted writes. It usually has something to do with the unassigned space, which isn't blocked by default because the Linux guys expected hidden capabilities in the devices. 

To solve this, cloud providers should have the ability to mask PCIe config space writes through module parameters. Otherwise, audit support for config space accesses to unassigned regions. Vendors could also just not put bad registers in unassigned regions. In a cloud environment, trusted software isn't enough if there are literal hardware vulnerabilities. 

challenges -> prev sols, limitations of such, 