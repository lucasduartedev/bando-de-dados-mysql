
# Repositório de Estudos - MySQL

## Objetivo

Esse repositório busca mostrar técnicas básicas de desenvolvimento de banco de dados _MySQL_ e uso de comandos SQL, não buscando solucionar problemas de desenvolvimento do mundo real.

<!-- # Projeto para prática de SQL com banco de dados MySQL -->

## Ferramentas

- **Editor de texto:** VSCode
- **Virtualização:** Docker (para manter o banco de dados)
- **Base de dados:** MySQL v9.0.1



## Na prática

- *__Docker__*

O _Docker_ será usado para virtualizar a base de dados MySQL.

É necessário baixar a imagem do banco de dados usando o terminal com o seguinte comando:

```
> docker pull mysql
```

Agora criaremos um container para manter nossa base de dados disponível:

```
> docker run --name nome_do_container -e MYSQL_ROOT_PASSWORD=senha -p 3306:3306 -d mysql
```

Para listar o container criado digite:

```
docker ps
```

Para acessar a base de dados via linha de comando:

```
docker exec -it nome_do_container mysql -p
```

*Observação: Irá solicitar a senha configurada pelo usuário.*


Ao acessar a base de dados MySQL, deixamos o contexto do Docker de lado e focaremos apenas no MySQL. 

<hr>

<!--

- *__MySQL__*

_Observações iniciais_

Para todo comando SQL busque usar 'ponto e vírgula' (;) ao final de cada comando. Isso indicará o final de cada instrução aplicada pelo usuário.

_Criar base de dados_

```
CREATE DATABASE `nome_base_de_dados`
CHARACTER SET utf8
DEFAULT COLLATE utf8_general_ci;
```

Ao criar a base de dados é necessário indicar ao gerenciador do banco de dados que queremos utilizar a base de dados desejada para realizar nossas manipulações.

_Selecionar base de dados_

```
USE nome_base_de_dados;
```

---------------------------------------  -->

<!-- _Criar tabela_ -->
