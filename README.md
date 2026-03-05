
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
> docker run --name NOME_DO_CONTAINER -e MYSQL_ROOT_PASSWORD=senha -p 3306:3306 -d mysql
```

Para listar o container criado digite:

```
docker ps
```

Para acessar a base de dados via linha de comando:

```
docker exec -it NOME_DO_CONTAINER mysql -p
```

*Observação: Irá solicitar a senha configurada pelo usuário.*


Ao acessar a base de dados MySQL, deixamos o contexto do Docker de lado e focaremos apenas no MySQL. 

<hr>


- *__MySQL__*

_Observações iniciais_

Para todo comando SQL busque usar 'ponto e vírgula' (;) ao final de cada comando. Isso indicará o final de cada instrução aplicada pelo usuário.

__Criar base de dados:__

```
CREATE DATABASE `nome_base_de_dados`
CHARACTER SET utf8
DEFAULT COLLATE utf8_general_ci;
```

Das três linhas de comando mostrada acima pode ser usada apenas a primeira linha para criar o seu banco de dados, desde que tenha o ponto e vírgula ao final da instrução. Já a segunda e terceira linha são opcionais, pois atribui algumas configurações de caracteres especiais, como acentuação.

__Listar base de dados existentes:__

```
SHOW DATABASES;
```

Nesse ponto será necessário indicar ao gerenciador do banco de dados que queremos usar uma base de dados em específica.

__Selecionar base de dados:__

```
USE nome_base_de_dados;
```

<hr/>

__Tipo de dados__

Para armazenar os dados é necessário definir o tipo, se é texto, numérico, entre outros.

- **Numéricos:**

- *Inteiro:* TyniInt, SmallInt, Int, MediumInt, BigInt;
- *Real:* Decimal, float, Double, Real;
- *Lógico:* Bit, Boolean.

- **Data/Tempo:**

- Date, DateTime, TimeStamp, Time, Year.

- **Literal:**

- *Caractere:* Char, Varchar;
- *Texto:* TinyText, Text, MediumText, LongText;
- *Binário:* TinyBlob, Blob, MediumBlob, LongBlob;
- *Coleção:* Enum, Set.

- **Espacial**

- Geometry, Point, Polygon, MultiPolygon.


