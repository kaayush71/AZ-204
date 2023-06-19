https://learn.microsoft.com/en-us/azure/app-service/overview

1. Zone redundancy is available for premium tiers. ( in this the app will be deployed in three data centres)
2. For deployment we can use something like github actions to do CI/CD pipelines.
3. Networking tab which is also enabled for premium tiers in which we can deploy our application to a VPC and setup firewalls and network security groups to access the resources.

### Main components when we deploy a web app
1. App service plan(know as server farm)
2. App service (know as site).
3. We can deploy multiple sites in a app service plan

### Scaling Policies
1. We have scale up (vertical scaling) and scale out (horizontal scaling) options here
2. For basic tier we have only manual scaling in scale out option but automatic scaling is available in premium tiers.

## Deployment Slots
1. Requires Standard or Premium plans
2. Maintain multiple version of the deployment like dev,qa,prod etc
3. Deployments can be swapped.
   for eg : dev deployment can be swapped with production deployment.


### Create a web app in Powershell
1. First create a resource group
2. Then create a web service plan
```shell
New-AzAppServicePlan -ResourceGroupName "powershellwebapp" -Name "azwebappserviceplan" -Location "EastUs" -Tier "Free"
```
3. Then create a web app
```shell
New-AzWebApp -ResourceGroupName "powershellwebapp" -Name "azwebapp" -Location "EastUs" -AppSerivcePlan "azwebappserviceplan"
```


### Create a web app using azure cli
1. Create a resource group
```bash
az group create --name cliwebapp --location eastus
```
2. Create app service plan
```bash
az appservice plan create -g cliwebapp -n mynewasp
```
3. create web app
```bash
az webapp create -g cliwebapp -n mynewwebapp -p mynewasp
```