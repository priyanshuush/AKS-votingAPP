
## Create K8s Cluster in AKS using Azure CLI

```
az aks create \
    --resource-group myResourceGroup \
    --name myAKSCluster \
    --node-count 2 \
    --generate-ssh-keys \
    --attach-acr <acrName>
```

### Install the Kubernetes CLI

To connect to the Kubernetes cluster from your local computer, you use `kubectl`, the Kubernetes command-line client.

If you use the Azure Cloud Shell, `kubectl` is already installed. You can also install it locally using the `az aks install-cli` command:

```
az aks install-cli
```

### Connect to cluster using kubectl

##### Azure CLI

To configure `kubectl` to connect to your Kubernetes cluster, use the `az aks get-credentials` command. 

```
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
```
To verify the connection to your cluster run:

```
kubectl get nodes
```
---


