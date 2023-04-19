# Sessão 03 - Criando imagens e avançando em containers

## Criando imagens e avançando em containers

Imagens são originadas de arquivos que programamos, é uma estrutura que determina ações que deverão ser realizadas.

hub.docker.com

## Criando a imagem

- from -> imagem base
- workdir -> diretório da aplicação
- expose -> porta da aplicação
- copy -> quais arquivos precisam ser copiados

Dockerfile

```docker
FROM node

WORKDIR /

COPY package*.json .

RUN npm install

COPY . . # copia os demais arquivos

EXPOSE 3000

CMD ["node", "app.js"]
```

Para fazer o build da imagem na pasta do Dockerfile:

> docker build .

> docker image ls

> docker run -d -p 3000:3000 --name aplicacao_node <id que foi gerado da imagem> 

Listar as imagens
> docker ps

## Alterando a imagem

O build terá que ser feito novamente.

## Camadas das imagens

As imagens são divididas em camadas (layers)

Caso uma nova diretriz seja passada no Dockerfile, mantém em cache para torná-lo mais performártico.

## Download de imagens

Deixar uma imagem disponível em nosso ambiente para ser utilizada posteriormente
> docker pull <nome da imagem>

## Mostrar mais informações sobre os comandos

Usar a flag --help
> docker run --help

## Múltiplas aplicações, mesmo container

> docker run -d -p 4000:3000 --name aplicacao_node1 <id que foi gerado da imagem> 
> docker run -d -p 5000:3000 --name aplicacao_node2 <id que foi gerado da imagem> 
> docker run -d -p 6000:3000 --name aplicacao_node3 <id que foi gerado da imagem> 

## Alterando o nome da imagem e tag

> docker tag <id> nomedaimagem

> docker tag <id> nomedaimagem:nomedatag

## Nomeando imagem no build

Na pasta do Dockerfile, utilizando a flag -t:

> docker build -t nomedaimagem .

Para listar as imagens:

> docker ps 

> docker build -t nomedaimagem:nomedatag .

## Reiniciando com interatividade

> docker start -i <id>

## Removendo imagens

Flag -f para forçar a remoção:

> docker rmi <imagem>

## Remover imagens, containers e networks não utilizados

> docker system prune

## Remover container automaticamente após a sua utilização

> docker run -d -p 6000:3000 --name aplicacao_node1 --rm <id>

> docker stop <container id>

Para visualizar as imagens criadas: 
> docker ps -a

## Copiando arquivos entre containers


