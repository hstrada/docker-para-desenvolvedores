# YAML

É uma linguagem de serialização. Usada geralmente para arquivos de configuração.

Extensão dos arquivos é yml ou yaml.

## Criando o arquivo

Chaves e valores;

## Espaçamento e identação

O fim de uma linha indica o fim de uma instrução

```yaml
nome: "Helena"
idade: x

objeto:
    versao: 2
    arquivo: teste.txt
```

## Comentários

Podem ser adicionados com o símbolo *#*

```yaml
# Instruções
nome: "Helena"
idade: x

# Objeto descreve o projeto
objeto:
    versao: 2
    arquivo: teste.txt
```

## Dados numéricos

Inteiros = 12

Floats = 15.8

```yaml
versao: 2
versao_completa: 2.14
```

## Strings

Com ou sem aspas

```yaml
texto_valido: "Digite um texto"
texto_valido_tambem: Digite um texto
```

## Dados nulos

*~* ou *null*

```yaml
nulo: ~
nulo_null: null
```

## Booleanos

```yaml
booleano: True/False
boolean_on_off: On/Off
```

## Listas

```yaml
lista: [1, 2, 3]
lista_opcao:
    - 1
    - 2
    - 3
```

## Dicionários (objetos ou listas com chave/valor)

```yaml
objeto: {a: 1, b: 2}
objeto_opcao:
    a: 1
    b: 2
```
