----

https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction

## Azure Storage data services

The Azure Storage platform includes the following data services:

- [Azure Blobs](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction): A massively scalable object store for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2.
- [Azure Files](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction): Managed file shares for cloud or on-premises deployments.
- [Azure Elastic SAN](https://learn.microsoft.com/en-us/azure/storage/elastic-san/elastic-san-introduction) (preview): A fully integrated solution that simplifies deploying, scaling, managing, and configuring a SAN in Azure.
- [Azure Queues](https://learn.microsoft.com/en-us/azure/storage/queues/storage-queues-introduction): A messaging store for reliable messaging between application components.
- [Azure Tables](https://learn.microsoft.com/en-us/azure/storage/tables/table-storage-overview): A NoSQL store for schemaless storage of structured data.
- [Azure managed Disks](https://learn.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview): Block-level storage volumes for Azure VMs.

### Access Tier
1. Hot
2. Cold
3. Arctic
4. Premium

## Networking
1. By default it is publicly available.
2. we can make it private or from a VPC.
3. Has support for private endpoint as well.

## Data Protection
1. Soft delete option ( need to wait for some day before the data inside the container will be deleted. )
2. Has Tracking/Versioning options as well.

## Encryption
1. Microsoft managed key / Customer managed key.
2. For customer managed key we need to have azure key vault account.
3. Infrastructure encryption is second level of encryption.

## SAS Token
1. We can generate sas (shared access signature) to provide access to a specific file inside blob storage or complete container using SAS token.
2. In this we have a large variety of customization like we can give only read/write acess or we can access to a specifi IP or for a particular time frame etc.
3. Sas tokens are valid till the acess key that we have used to sign that sas token is valid.

## AZ-Copy
1. AzCopy is a command-line utility that you can use to copy blobs or files to or from a storage account. 
2. It can be used to copy a file from one container into another.
3. We can use SAS token or Azure-AD(active directory) to copy file from one container to another.
