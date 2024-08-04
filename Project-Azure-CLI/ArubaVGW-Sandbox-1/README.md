# Lab - Aruba Virtual Gateway Sandbox 1

## Intro

To be able to deploy the bare minimal requirements for an Aruba VGW.

![net diagram](./Media/arubavgw-orchestrate-sandbox-example-1.png)

```bash
wget -O ArubaVGW-Orchestrate-Sandbox.sh https://raw.githubusercontent.com/CyberOps-Ninja/Azure-IaC/main/Project-Azure-CLI/ArubaVGW%20Sandbox-1/ArubaVGW-Orchestrate-Sandbox.azcli
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