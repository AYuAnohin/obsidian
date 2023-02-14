Call позволяет вызвать метод в контексте другого объекта.
```js
let worker1 = {
  name: 'Oleg',
  sayHello(from){
    console.log(this.name + ' delivery hello from ' +  from)
  }
}

let worker2 = {
  name: 'Olga',
}

worker1.sayHello('it') //Oleg delivery hello from it
worker1.sayHello.call(worker2, 'gg') //Olga delivery hello from gg
```

#programming/web/frontend/js