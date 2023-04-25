# Gerenciando múltiplos containers com docker compose

## Docker Compose

É uma ferramenta para rodar múltiplos containers. Apenas um arquivo de configuração que orquestra os builds.

docker-compose.yml

*Coordenar os containers e imagens*

- version: versão do compose;
- services: containers/serviços que vão rodar a aplicação;
- volumes: possível adição de volumes;

## Rodando o compose

Para que as instruções nos arquivos sejam executadas:
> docker-compose up

## Rodando em background

> docker-compose up -d

## Parando o compose

> docker-compose down


