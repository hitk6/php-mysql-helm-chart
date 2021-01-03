# php-mysql-helm-chart

To launch the helm chart run this command

>> cd php-mysql-helm-chart

>> helm install mychart .

the chart will be deployed at port no 30007

if nginx ingress controller is enabled then port no will be 80

All the files are already in the docker image

/var/www/html contains

├── index.php

└── php-info.php

the environment variables of mysql database are by default written in index.php

So, the php code will automatically connect with mysql database 

autoscaling feature is included in chart for more details read the values.yaml file

# for autoscaling metrics server should be enabled

run this command to enable metrics server

>> kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/download/v0.3.7/components.yaml

the metrics-server pod will be deployed in namespace kube-system

kubectl get deployment metrics-server -n kube-system

# Enable nginx ingress controller

this command is for minikube k8s cluster

>> minikube addons enable ingress 
