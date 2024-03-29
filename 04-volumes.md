# Volumes

Todo dado criado por um container é salvo nele, logo quando o mesmo é removido, suas informações também serão.

Persistir dados em aplicações e não depender de containers pra isso. 

`Volumes são necessários para gerenciar os dados e fazer backup de forma mais simples.`

## Tipos de volumes

- Anônimos: flag -v -> nome aleatório;
- Nomeados: volumes com nomes;
- Bind mounts: salvar dados na máquina sem o gerenciamento do docker.

*Anônimos*
> docker run -v /data

*Nomeados*
> docker run -v nomedovolume:/data

Verificar volumes criados
> docker volume ls

*Bind mount*

Apontamos um diretório
> docker run /dir/data:/data

O diretório do computador informado (dir/data ou C:/) será o volume do container

## Criar um volume

> docker volume create <nome>

Para listar os volumes
> docker volume ls

Associando ao container
> docker run -d -p 80:80 --name <nomecontainer> -v <nomedovolume>:<diretorio>

## Listando volumes

> docker volume ls

## Inspecionando um volume

> docker volume inspect <nomedovolume>

## Removendo volumes

> docker volume rm <nomedovolume>

## Removendo volumes em massa

Remover volumes que não estão sendo utilizados
> docker volume prune

## Volume somente leitura

ro = read only
> docker run -v volume:/data:ro
