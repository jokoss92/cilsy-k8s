# cilsy-k8s
deploy nodejs application to k8s cluster on minikube local

# build and push nodejs image to registry
1. go to your home directory 
```
cd ~/

```

2. clone source code 
```

https://github.com/rizkyramadhanch/cilsy-api.git 
```

3. go to source code directory 
```
cd ~/cilsy-api
```

4. build your image
```
docker build -t <your image name>:[your tag name]
```

5. login to your docker hub
docker login -u <username> -p <your password>

6. push your image to registry
```
docker push <your image name>:[your tag name]
```


# deploy nodejs image to k8s cluster on minikube local
`1.install minikube on local
```
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install curl
sudo apt-get install apt-transport-https
sudo apt install virtualbox virtualbox-ext-pack
wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo chmod 755 /usr/local/bin/minikube
minikube version
minikube start
```

2. install kubectl command
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

3. cek information cluster k8s
```
kubectl config view
kubectl cluster-info
kubectl get nodes
```
4. deploy all yaml file on this folder repository with kubectl command
```
kubectl create -f <.yaml>
```
