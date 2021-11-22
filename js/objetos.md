### Objetos

Um objeto é uma coleção de dados guardadas em um váriavel com chaves e valores.

<br />

```js
// Criando um objeto
const pessoa = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
}

// Acessando os dados por notação de ponto:
console.log(pessoa.nome); // João

// Acessando os dados por notação de colchetes:
console.log(pessoa['idade']); // 20
```

<br />

#### Destructuring

Serve para desestruturar objetos.

<br />

```js
const pessoa = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
}

// Os dados agora estão separados em cada variavel
const { nome, idade, cidade } = pessoa;

console.log(cidade); // São Paulo
```

#### Array de objetos

```js
// Um array de objetos
const filmes = [
    {
        titulo: "Dilema das Redes",
        descricao: "Um documentario sobre tecnologia"
    },
    {
        titulo: "Us",
        descricao: "Um filme de terror"
    }
];

const [{ titulo, descricao }] = filmes;

filmes.map(filme => console.log(filme.titulo));
// Dilema das Redes
// Us
```