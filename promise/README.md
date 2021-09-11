# Promise
É um objeto usado para processamento assíncrono. Uma `promise` representa uma ação que pode estar disponível agora, no futuro ou nunca. 

Uma `promise` possuirá um destes estados: 
- `pending`: nem realizada, nem rejeitada. 
- `fulfilled`: realizada
- `rejected`: rejeitada ou falhada

```js
const defer = new Promise((resolve, reject) => {
  setTimeout(() => {
    if (true) {
      resolve('Hello! It works!')
    } else {
      reject('Error!')
    }
  }, 4000)
})

defer
  .then((data) => {
    console.log(data)
    return 'foo'
  })
  .then((data) => console.log(data))
  .catch((error) => console.log(error))
```

```js
const currency = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve({ currency: 'euro', value: 3.50 })
    }, 3000)
  })

  const countries = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(['Ireland', 'England', 'Scotland'])
    }, 300)
  })

  Promise
    .all([currency, countries])
    .then((responses) => console.log(responses))

  Promise
    // First promise resolve
    .race([currency, countries])
    .then((responses) => console.log(responses))
```