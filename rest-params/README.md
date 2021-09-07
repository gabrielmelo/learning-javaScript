# Rest params

Permite representar um número indefinido de argumentos como um array. Se o último argumento de um função tiver o prefixo `...` ele irá se tornar um array. Ideal para quando não sabemos quantos argumentos serão passados em um função

```js
const multiply = (multiplier, ...numbers) => {
  return numbers.map(number => multiplier * number)
}

console.log(multiply(2, 2, 4, 6)) // > Array(3) [ 4, 8, 12 ]
```