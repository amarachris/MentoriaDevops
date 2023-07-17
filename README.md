# MentoriaDevops

Auxiliar os inciantes a montar o melhor ambiente de estudo.

### Segue os links de referência:

Você vai precisar do Docker: https://docs.docker.com/engine/install/ubuntu/

### Segue as instalações e o passo-a-passo em ordem

### Marcar o DNS no host do Server:
````
curl -4 icanhazip.com
````
### Direcionar ao seu provedor de DNS e crie um registro :
````
dig +short replace_with_subdomain
````
### Pacotes de atualização e pré-requisitos de instalação
````
sudo apt-get update && sudo apt upgrade -y
sudo apt-get -y install gnupg2 ca-certificates curl apt-transport-https iptables
````
### Instalar Helm V3
Additional Information - https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
````
Additional Information - https://helm.sh/docs/intro/install/
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
```
````
### Instalar kubectl
Additional Information - https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
````
sudo apt update
sudo apt install ca-certificates curl apt-transport-https -y
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt update
sudo apt install kubectl -y
````
```
````
### Instalar Minikube
Additional Information - https://minikube.sigs.k8s.io/docs/start/
````
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start --extra-config=kubeadm.ignore-preflight-errors=NumCPU --force --cpus 1
