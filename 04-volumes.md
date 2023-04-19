# Volumes

Todo dado criado por um container é salvo nele, logo quando o mesmo é removido, suas informações também serão.

Persistir dados em aplicações e não depender de containers pra isso. 

`Volumes são necessários para gerenciar os dados e fazer backup de forma mais simples.`

## Tipos de volumes

- Anônimos: flag -v -> nome aleatório;
- Nomeados: volumes com nomes;
- Bind mounts: salvar dados na máquina sem o gerenciamento do docker.
