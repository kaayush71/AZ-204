https://azure.microsoft.com/en-in/products/virtual-machines
1. Has availability options while creating.
	> Availability zone
	> Virtual machine scale set
	> Availability set
2. Supports wide variety of images.
3.  Supports for Linux distribution as well.
4. Spot instance
5. Has 568 size options for storage.  ( B and D are in general purpose )
6. Windows machine requires a administrator account and for Linux its public private key pair.
### For encryption
1. Keys are stored in azure key vault.
2. We can have platform managed,customer managed or both type of keys.

### For disks 
1. We can enable ultra disk compatibility for very fast read and rights but it need to be deployed in Availability zones.
2. We can also attach external disks in virtual machine. ( **Data Disks** ) 

## Networking

1. We have to create virtual network,subnet and public IP for the instance .