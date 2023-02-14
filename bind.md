Метод bind привязывает this к определенному контексту.
Это бывает необходимо когда мы вынуждены пробрасывать метод объекта без вызова, сейчас функционал bind в большинстве своем заменила [[Стрелочная функция js]]
Метод bind возвращает новую функцию.
```js
let admin = {
  name: 'Oleg',
  greetings(from){
    console.log(this.name + ' hello ' + from)
  }
}

setTimeout(admin.greetings, 1000) //undefined hello undefined
setTimeout(admin.greetings.bind(admin, 'from it'), 1000) //Oleg hello from it
setTimeout(()=>{
  admin.greetings('from it')
}, 1000) //Oleg hello from it
```

#programming/web/frontend/js