# Destructuring assignment

Atribuição via desestruturação é uma expressão JavaScript que possibilita extrair dados de um array ou objeto.

## Objects
```js
let data = {
  name: 'Gabriel',
  surname: 'Melo',
  nickname: 'gabsmelo',
  age: 33,

  social: {
    twitter: '@gblmlo',
    facebook: '/gabsmelo'
  }
}

let { name } = data;
let { twitter, facebook } = data.social;

console.log(data)
console.log(name) // > Gabriel
console.log(twitter, facebook) // > @gabsmelo 
```

## Array

```js
let arr = ['Gabriel', 'Melo', 33]

let [ name, surname, age ]

console.log(name, surname, age) //> Gabriel Melo 33
```

## Swap variables
Os valores de duas variáveis podem ser trocados em uma expressão de desestruturação.

```js
let a = 20;
let b = 42;

[a, b] = [b, a];
console.log('a:', a) // > 42
console.log('b:', b) // > 20
```