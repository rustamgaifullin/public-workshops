# Setup your local environment

## Important
Backup your ~/.kube directory!!!!

Latest version of minikube binary did not work for me so I pinned to 1.3.1

Original instructions at https://kubernetes.io/docs/tasks/tools/install-minikube/


## Install the dependencies (Linux)

```
sudo apt-get update
sudo apt install virtualbox

curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.3.1/minikube-linux-amd64 && chmod +x minikube && sudo cp minikube /usr/local/bin/ && rm minikube

curl -Lo kubectl https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /usr/local/bin/

minikube start --vm-driver=virtualbox
```

## Install the dependencies (osx)

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.3.1/minikube-darwin-amd64 && chmod +x minikube && sudo cp minikube /usr/local/bin/ && rm minikube
brew install kubernetes-cli
minikube start --vm-driver=virtualbox
```

## Summary

In this lab your learned how to bootstrap a kubernetes using minikube
