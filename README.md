# MentoriaDevops
Auxiliar os inciantes a montar o melhor ambiente de estudo.

Segue os links de referência:
````
Você vai precisar do Docker: https://docs.docker.com/engine/install/ubuntu/
Minikube: https://minikube.sigs.k8s.io/docs/start/
### Install Helm v3
Additional Information - https://helm.sh/docs/intro/install/
````
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
````

### Install kubectl
Additional Information - https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
````
sudo apt update
sudo apt install ca-certificates curl apt-transport-https -y
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt update
sudo apt install kubectl -y
