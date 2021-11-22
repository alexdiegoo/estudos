### Arrays no Js

Array é uma coleção de elementos em uma única variável.
<br />

```js
// Criando um array:
const frutas = ["Laranja", "Banana", "Uva"];

//Acessar informações de um array:
console.log(frutas[0]) // Laranja
// O primeiro elemento de um array é o índice 0
```

#### Operador spread
O operador spread "espalha" os elementos de um array em outro array.

<br />

```js 
// Criando um array:
const frutas = ["Laranja", "Banana", "Uva"];

// Copiando os elemento do array frutas em outro array:
const outrasFrutas = [...frutas, "Maçã", "Limão"];

console.log(outrasFrutas); // ["Laranja", "Banana", "Uva", "Maçã", "Limão"];
```

#### Metodos de iteração

**1 - Map:** retorna um novo array sem alterar o array original criando uma cópia com as alterações que desejamos.

<br />

```js
const alunas = ["Paula", "Maria", "Estela", "Clara"];

// O map espera uma callback
alunas.map(aluna => console.log(aluna));
```

<br />

**2 - Filter:** retorna um novo array com os elemento filtrados.

<br />

```js
const numeros = [34, 35, 67, 90, 55, 76];

// O filter espera uma callback
const numerosPares = numeros.filter(numero => numero % 2 == 0);

console.log(numerosPares); // [34, 90, 76]
```

<br />

**3 - Find:** encontra e retorna o primeiro elemento que achar igual ao elemento passado por parâmetro.

<br />

```js
const produtos = ["Geladeira", "Fogão", "Cama", "Mesa"];

// O find espera uma callback
const encontraCama = produtos.find(produto => produto === "Cama");

console.log(encontraCama); // Cama

// Se o elemento não existir retorna undefined
```

<br />

**4 - Sort:** ordena o array

<br />

```js
const num = [34, 45, 76, 90, 55];

// O sort espera uma callback, se não for passada ele ordena em ordem crescente.

console.log(num.sort()) // [34, 45, 55, 76, 90]

// Mas existe um problema, ele utiliza apenas o primeiro numero para ordenação.
```

<br />

**5 - Reduce:** reduz array a um resultado de uma operação matemática.

<br />

```js
const num = [1, 34, 35];

// o reduce espera uma callback
const soma = num.reduce((valorAnterior, valorAtual) => {
    return valorAnterior + valorAtual;
});

console.log(soma); // 70
```