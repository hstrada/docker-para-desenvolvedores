# Kubernetes

Ferramenta para osquestração de containers.

Permite a criação de múltiplos containers em diferentes máquinas;

## Conceitos

- Control Plane -> gerenciamento o controle dos processos dos Nodes
- Nodes -> máquinas gerenciadas pelo Control Plane;
- Deployment -> execução de uma imagem em um Pod;
- Pod -> um ou mais containers que estão em um Node;
- Services -> serviços que expõe os Pods ao mundo externo;
- kubectl -> cliente de linha de comando para o Kubernetes.

## Dependências

kubectl & Minikube (simulador)

## Inicializar o minikube

minikube start --driver=<driver>

> minikube start --driver=docker

## Acessando a dashboard

> minikube dashboard

## Outros comandos

> kubectl get pods

> kubectl describe pods

> kubectl config view

> kubectl expose deployment <nome> --type=<tipo> --port=<port>

> minikube service <nome> -> ip aparece no terminal

> kubectl get services

> kubectl scale deployment/<nome> --replicas=<numero> -> replicar a aplicação

> kubectl get pods

> kubectl get rs -> verificar o número de réplicas

> kubectl scale deployment/<nome> --replicas=<numero_menor> -> diminuir o número de réplicas

> kubectl rollout undo deployment/<nome> -> desfazer uma atualização

> kubectl delete service <nome> -> deletar um serviço

> kubectl delete deployment <nome> -> deletar um deployment

## Modos

### Imperativo 

Por comandos

### Declarativo

Por arquivo

## Chaves

- apiVersion: versão da ferramenta;
- kind: tipo do arquivo (deployment, service);
- metadata: descrever algum objeto;
- replicas: número de réplicas de Nodes;
- containers: especificações dos containers.


