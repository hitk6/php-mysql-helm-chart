# php-mysql-helm-chart

To launch the helm chart run this command

cd php-mysql-helm-chart

helm install mychart .

the chart will be deployed at port no 30007

if nginx ingress controller is enabled then port no will be 80

All the files are already in the docker image
/var/www/html contains
├── index.php

└── php-info.php

the environment variables of mysql database are by default written in index.php

So, the php code will automatically connect with mysql database 


