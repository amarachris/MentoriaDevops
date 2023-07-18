<h1 align="center"> MentoriaDevops </h1>

<p align="center">
<img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge"/>
</p>

> :construction: Projeto em construção :construction:

Auxiliar os inciantes a montar o melhor ambiente de estudo.

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
Link- https://helm.sh/docs/intro/install/
````
Additional Information - https://helm.sh/docs/intro/install/
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
````
### Instalar kubectl
Link- https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
````
sudo apt update
sudo apt install ca-certificates curl apt-transport-https -y
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt update
sudo apt install kubectl -y
snap install kubectl --classic
````
### Instalar Minikube
Link - https://minikube.sigs.k8s.io/docs/start/
````
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start --extra-config=kubeadm.ignore-preflight-errors=NumCPU --force --cpus 1
````
### Instalar Docker
Link - https://docs.docker.com/engine/install/ubuntu/
````
 sudo apt-get update
 sudo apt-get install ca-certificates curl gnupg
 sudo install -m 0755 -d /etc/apt/keyrings
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
 sudo chmod a+r /etc/apt/keyrings/docker.gpg
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
 sudo apt-get update
 sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
````
### Subir container e vamos estar usando o Portainer como teste
Link - https://docs.portainer.io/start/install-ce/server/docker/linux
````
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
````
### Vamos instalar GUI e também um server para acesso remoto do nossa instância
Link - https://bytexd.com/x2go-ubuntu/
````
sudo apt update
sudo apt install x2goserver x2goserver-xsession
sudo apt install lxde
