[Official Link](https://learn.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview)

Azure managed disks are block-level storage volumes that are managed by Azure and used with Azure Virtual Machines. Managed disks are like a physical disk in an on-premises server but, virtualized. With managed disks, all you have to do is specify the disk size, the disk type, and provision the disk. Once you provision the disk, Azure handles the rest.

### Highly durable and available

## Disk roles

There are three main disk roles in Azure: the data disk, the OS disk, and the temporary disk. These roles map to disks that are attached to your virtual machine.

**Os disk** : Every virtual machine has one attached operating system disk. That OS disk has a pre-installed OS, which was selected when the VM was created. This disk contains the boot volume.

**Temporary disks** : Most VMs contain a temporary disk, which is not a managed disk. The temporary disk provides short-term storage for applications and processes, and is intended to only store data such as page files, swap files, or SQL Server tempdb.

**Data disks** : A data disk is a managed disk that's attached to a virtual machine to store application data, or other data you need to keep.

![[Azure Disk Roles.png]]

### Private Links
Private Link support for managed disks can be used to import or export a managed disk internal to your network.