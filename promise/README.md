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
