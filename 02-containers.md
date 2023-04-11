# Sessão 02

## Trabalhando com Containers

Executar uma imagem em um container:
> docker run imagem

Verificar containers sendo executados:
> docker ps ou docker container ls

Verificar quais já foram executados na máquina:
> docker ps -a
> docker container ls -a

Executar um container com interação:
> docker run -it ubuntu

Executar em background (detached):
> docker run -d  ubuntu

Expor portas:
> docker run -d -p 3000:80 nginx

Expondo no pc:expondo no container (localhost:3000)

Parar container:
> docker stop <id ou nome>

Iniciar um container (não precisa criar um container):
> docker start <id> 

Definindo o nome de um container:
> docker run -d -p 80:80 --name nginx_app nginx

Verificando os logs de um container:
> docker logs <id>

Ficar sempre apresentando os logs:
> docker logs -f <id>

Remover um container da máquina:
> docker rm <id>

Forçar a remoção, ainda que ele esteja sendo executado:
> docker rm <id> -f

Listar todos os containers:
> docker ps -a && docker rm <id ou nome>

## Criando imagens e avançando em containers

Imagens são originadas de arquivos que programamos, é uma estrutura que determina ações que deverão ser realizadas.

