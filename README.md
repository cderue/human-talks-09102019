# human-talks-09102019

# Create a resource group

`az group create --name human-talks-rg --location westeurope`

# Create an AKS cluster

az aks create \
    --resource-group human-talks-rg \
    --name human-talks-aks \
    --node-count 1 \
    --enable-addons monitoring \
    --generate-ssh-keys
    
# Connect to the cluster

`az aks get-credentials --resource-group human-talks-rg --name human-talks-aks`
