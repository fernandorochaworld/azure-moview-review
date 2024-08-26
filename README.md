# DevOps4Devs 

## Aula 01
### O projeto conversão de temperatura se encontra no link abaixo:

[https://github.com/KubeDev/conversao-temperatura](https://github.com/KubeDev/conversao-temperatura)

## Aula 02
### Comando de criação do cluster Kubernetes com o K3D
```bash
k3d cluster create meucluster --servers 3 --agents 3 -p "30000:30000@loadbalancer"
```

### Connection String 

```
Host=postgres;Database=reviewvideo;Username=reviewvideo;Password=Passw0rd2024!
```

## Aula 03

### Cadastro no Azure

[https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account](https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account)

### Instalação do Azure CLI

[https://learn.microsoft.com/en-us/cli/azure/install-azure-cli](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)


# Azure

#### Install Azure CLI

curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
az --version

#### Login

az login

#### Connection
az account set --subscription \<hash-id\>
az aks get-credentials --resource-group aula-k8s_group --name aula-k8s --overwrite-existing

#### Publish new image

docker build -t fernandorochaworld/azure-movie-review:v1.0.0 -f ./Review-Filmes.Web//Dockerfile --push .

#### Apply deployment

kubectl apply -f k8s/deployment.yaml

