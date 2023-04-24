# Networks

Uma forma de gerenciar a conexão do docker, são separadas dos containers. Torna-se simples a comunicação entre containers;

## Tipos de conexão

Externa -> conexão com uma API de um servidor externo;

Host -> comunicação com a máquina que está executando o Docker;

Entre containers -> comunicação que utiliza o driver bridge e permite a comunicação entre dois ou mais containers.

## Tipos de driver

Bridge -> containers precisam se comunicar (mais comum);

host -> conexão entre o container e a máquina;

macvlan -> permite a conexão a um container por um MAC address;

none -> remove todas as conexões de rede de um container;

plugins -> permite extensões de terceiros para criar outras redes;

## Listando networks

> docker network ls

## Criando redes

Criando tipo bridge
> docker network create <nome>

Criar tipo macvlan
> docker network create -d macvlan minharedemacvlan

## Removendo redes

> docker network rm <nome>

## Removendo redes em massa

Todas as redes não utilizadas serão removidas
> docker network prune

## Conectar container

> docker network connect <rede> <container>

## Desconectar container

> docker network disconnect <rede> <container>

## Inspecionando redes

> docker network inspect <nome>


