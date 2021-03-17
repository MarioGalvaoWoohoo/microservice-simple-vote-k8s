# microservice-simple-vote-k8s
Sistema simples de voto com k8s e micro services


Localmente trabalhado com Minikube

step by step

minikube start (cria um cluster)

kubectl create -f namespaces/ --save-config --record (Cria o namespace)
kubectl create -f deployments/ --save-config --record (Cria o deployments)
kubectl create -f services/ --save-config --record (Cria o service)

Localmente nao funciona o LoadBalance, mas se disponibilizar em algum serviço na nuvem "aws, Google Cluod, Azure ..." funionará fazendo as seguintes alterações...

Alterar o type no spec dos serviços de result.yaml e vote.yaml , onde atualmente esta como NodePort para LoadBalancer e remover a linha nodePort: 31000 e nodePort: 31001
