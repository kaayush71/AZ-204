https://azure.microsoft.com/en-in/products/virtual-machines
1. Has availability options while creating.
	> Availability zone
	> 	[Availability zones](https://learn.microsoft.com/en-us/azure/availability-zones/az-overview?context=/azure/virtual-machines/context/context) expands the level of control you have to maintain the availability of the applications and data on your VMs. An Availability Zone is a physically separate zone, within an Azure region. There are three Availability Zones per supported Azure region.
	> 	
	> Virtual machine scale set
	> 	[Azure virtual machine scale sets](https://learn.microsoft.com/en-us/azure/virtual-machines/flexible-virtual-machine-scale-sets) let you create and manage a group of load balanced VMs. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule.
	> 
	> Availability set
	> 	An [availability set](https://learn.microsoft.com/en-us/azure/virtual-machines/availability-set-overview) is a logical grouping of VMs that allows Azure to understand how your application is built to provide for redundancy and availability.
	
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

## Load Balancing
1. None
2. Azure load balancer (Network load balancer)
3. Application gateway (Application load balancer)

## Connect to Vm
1. RDP
2. SSH
3. Bastion

## ARM (Azure resource manager) templates
1. They can also be used to deploy your virtual machine.
2. when we want to deploy a large number of machines then we can use this script and pass custom parameters in parameters.json file and run this script multiple times.

## Create VM using cloudshell

### to create a resource group 

```shell
New-AzResourceGroup -Name pwrsgroup -Location 'EastUS'
``` 

### to create a vm
```shell
New-AzVM -ResourceGroupName 'pwrsgroup' -Location 'EastUS' -Name 'pwrsdemo' -PublicIpAddressName 'myPublicIP' -OpenPorts 80,443,3389 
```


## Create VM using powershell

### to create a resource group 

``` shell
New-AzResourceGroup -Name powershellgrp -Location EastUS
``` 

### to create a vm
```shell
New-AzVM -ResourceGroupName powershellgrp -Name aznewvm -Location EastUs -VirtualNetworkName "mynewVNet" -SubnetName "default" -SecurityGroupName "nynewNSG" -PublicIpAddressName "mypublicip" -OpenPorts 80,3389
```
when using powershell we need to create virtual-network ,subnet and security-group.

## Create VM using Azure Cli

### to create a resource group

```shell
az group create --name cligroup --location eastus
```

### to create a vm

```shell
az vm create --resource-group --name aznewvm --image win2016datacenter --admin-username azdjdtestuser
```