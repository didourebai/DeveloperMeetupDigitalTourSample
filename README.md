# DeveloperMeetupDigitalTourSample
This is the sample for developer meetup digital tour 

## Create Azure Container Registry 
We can create a registry using either the Azure portal, or the acr create command in the Azure Command Line Interface (CLI)
```sh
$az acr create --name myregistry --resource-group mygroup --sku standard --admin-enabled true
```
## Deploy the application on Azure Container Registry
1- In our local command prompt, we will run the following command, replacing <registry-name> with the name of your container registry, to tag the current image with the name of your registry.
```sh
$ docker tag myacrsample:latest <registry-name>.azurecr.io/myacrsample:latest
```
## Create AKS cluster using Azure CLI
 ```sh
$ az aks create --resource-group aksgr --name myAKSClusterName --node-count 1 -- generate-ssh-keys --attach-acr yourContainerName
 ``` 
  
