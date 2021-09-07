# Spread Operator
Permite desmembrar qualquer elemento iterável em elementos literais e parâmetros individuais.

**Use 1**
```js
const front = ['html', 'css', 'js']
console.log(front)
console.log('Spread operator: ', ...front)
```

**Use 2**
```js
const makeSandwich = (bread, cheese, souce) => console.log(`Your sandwich with: ${bread} bread, ${cheese} cheese and ${souce} is done!`)

const ingredients = ['white', 'cheddar', 'barbecue']
makeSandwich(...ingredients)
```

