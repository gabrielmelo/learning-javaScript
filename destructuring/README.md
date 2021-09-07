# Destructuring assignment

Atribuição via desestruturação é uma expressão JavaScript que possibilita extrair dados de um array ou objeto.

## Objetos
```javascript
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

```javascript
let arr = ['Gabriel', 'Melo', 33]

let [ name, surname, age ]

console.log(name, surname, age) //> Gabriel Melo 33
```