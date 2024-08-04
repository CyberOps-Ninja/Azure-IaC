# Lab - Aruba Virtual Gateway Sandbox 1

## Intro

To deploy the bare minimal requirements in Azure for an Aruba VGW using Azure CLI and Aruba Central Virtual Gateway platform. Code contains Resource Group, Virtual Network, Subnet, Network Security Group, and SSH Key pair.

![net diagram](./Media/arubavgw-orchestrate-sandbox-example-1.png)


### Deploy this solution

The lab is also available in the above .azcli that you can rename as .sh (shell script) and execute. You can open [Azure Cloud Shell (Bash)](https://shell.azure.com) and run the following commands build the entire lab:


```bash
wget -O ArubaVGW-Orchestrate-Sandbox.sh https://raw.githubusercontent.com/CyberOps-Ninja/Azure-IaC/main/Project-Azure-CLI/ArubaVGW-Sandbox-1/ArubaVGW-Orchestrate-Sandbox.azcli
chmod +xr ArubaVGW-Orchestrate-Sandbox.sh
./ArubaVGW-Orchestrate-Sandbox.sh
```

### Default Parameters:

```bash
# Parameters (Can be changed and should be changed to prevent any overlay in your environment)
rg="RG-ArubaVGW-IaC"
location="eastus"
vnetname="VNet-ArubaVGW"
address_prefix="10.181.0.0/16"
subnetname="Azure-Services-Subnet"
subnet_prefix="10.181.1.0/24"
nsgname="NSG-ArubaVGW"
sshkeyname="ssh-key-arubavgw-sandbox"
```


### Clean-up

```bash
# Parameters 
rg=RG-ArubaVGW-IaC

# Clean up
az group delete -g $rg --no-wait 
```