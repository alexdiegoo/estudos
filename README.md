### Meus estudos 🧠
#### Git e GitHub
Comandos: 
- `git init`: inicia nosso versionamento.
- `git add`: adiciona ou modifica alterações elegíveis para nosso ponto no tempo.
- `git commit`: adiciona nosso ponto na linha do tempo.
- `git log`: visualiza os pontos na linha do tempo (commit).
- `git status`: informa estado atual de alterações.
- `git show`: apresenta um ponto indicado na linha do tempo.
- `git branch`: gerencia nossa realidades alternativas.
- `git checkout`: navega entre nossas realidades alternativas.
- `git merge`: une nossas linhas do tempo.
- `git push`: envia nossas alterações para um repositório remoto (github).
- `git clone`: clonar um repositório.
- `git pull`: atualiza o repositório local apartir do remoto.

GitFlow: É uma metodologia que consiste em separar o projeto em branch (master, hotfix, realese, feature) para gerenciar melhor o projeto.

#### MySQL
Para mostrar todos os bancos de dados do MySQL:

```sh

SHOW DATABASES;

```
<br />
Para criar um banco de dados:

```sh

CREATE DATABASE nome-do-banco;

```

<br />
Para acessar o banco de dados:

```sh

USE nome-do-banco;

```

<br />
Mostra todas as tabelas de um banco de dados:

```sh

SHOW TABLES;

```

<br />
Para criar uma tabela, dentro dos parenteses é definido o nome da coluna e seu tipo e a quantidade de caracteres.

```sh

CREATE TABLE nome-da-tabela (
  nome VARCHAR(50),
  email VARCHAR(100),
  idade INT
)

```

<br />
Para ver a estrutura da tabela:

```sh

DESCRIBE nome-da-tabela;

```

<br />
Para inserir dados em um banco de dados:

```sh

INSERT INTO nome-da-tabela(nome, email, idade) VALUES(
   "Alex Diego",
   "teste@email.com",
   18
);

```

<br />
Para listar todos os dados de uma tabela:
Ou com alguma condição especifica:

```sh

SELECT * FROM nome-da-tabela;

SELECT * FROM nome-da-tabela WHERE idade = 18;

```

<br />
Para deletear registro dentro de uma tabela SEMPRE USAR WHERE

```sh

DELETE FROM nome-da-tabela WHERE nome = "Alex Diego";

```

<br />
Para atualizar um registro: SEMPRE USAR WHERE

```sh

UPDATE nome-da-tabela SET nome = "Nome de Teste", idade = 10 WHERE nome = "Alex Diego";

```

  
  
#### HTML5
- [Midia: Imagem, audio e video](https://github.com/alexdiegoo/estudos/blob/main/html5/midia.md)
#### CSS
- [Medidas CSS](https://github.com/alexdiegoo/estudos/blob/main/css/medidas.md)
#### JS
