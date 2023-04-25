# Orquestração de Containers

Gerenciar e escalas os containers da nossa aplicação.

Alguns serviços como: docker swarm, kubernetes e apache mesos.

## Docker Swarm

- Ferramenta para orquestrar containers. 
- Escalar horizontalmente [cluster].

## Conceitos

- Nodes: instância que participa do Swarm;
- Manager Node: gerencia os demais nodes;
- Worker Node: trabalham em função do manager;
- Service: conjunto de tasks que o Manager solicita para o work executar;
- Task: comandos que são executados nos nodes;

## AWS

EC2 -> rodar projetos web

Launch Instances

Free tier eligible

Na máquina, TCP, HTTP e SSH

Abre a instância, connect, SSH client

## Instalando o Docker

> sudo yum update -y

> sudo yum install docker

> sudo service docker start

## Iniciando o swarm

ssh para conectar
> sudo docker swarm init

A instância irá virar um Node;

## Listando nodes ativos

> docker node ls

## Adicionando máquinas no swarm

> docker swarm join --token <token> <ip>:<port>

Essa nova máquina entra como worker;

## Subindo um novo serviço

> docker service create --name <nome> <imagem>

## Listando serviços

> docker service ls

> docker node ls
Só a máquina leader consegue apresentar o conteúdo que está sendo executado

## Removendo serviços

> docker service rm <nome>

> docker service ls

## Replicando serviços

> docker service create --name <nome> --replicas <numero> <imagem>

> docker service create --name nginxreplicas --replicas 3 -p 80:80 nginx

## Verificando a orquestração

Mesmo que delete, apague, ele observa o evento e consegue recriar as instâncias.

## Checando token do swarm

> docker swarm join-token manager

## Checando o swarm

> docker info

## Removendo instância do swarm

Em um node:
> docker swarm leave

## Removendo um node

> docker node rm <id>

## Inspecionando serviços

> docker service inspect <id>

## Containers ativos pelo service

> docker service ps <id>

## Compose no swarm

> docker stack deploy -c <arquivo.yaml> <nome>

## Escalando a aplicação

> docker service ls

> docker service scale <nome>=<replicas>

## Atualizando imagem

> docker service ls

> docker service update --image nginx:1.18.0 <id>

## Criando redes

> docker network create --drive overlay swarm

> docker service create --name nginxreplicas --replicas 3 -p 80:80 nginx --network swarm nginx

## Atualizando a rede

> docker service update --network swarm <id>

> docker service update --network-add swarm <id>
