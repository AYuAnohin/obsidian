Proxy это объект оборачивающий 'target' объект. 

Proxy позволяет менять поведение 'target' объекта, путем перехватывания операций.
(Не все операции можно перехвотить, есть инваринты, которые служат для соблюдения стандартов языка) 

То есть по сути ты должен работать не с самим объектом, а с его оболочкой.(но Proxy должен заменять оригинальный объект собой, чтобы к оригиналу не было доступа)

```js
let admin = {
  name: ''
}
let handler = {
  get: (target, prop)=>{
    if(!target.prop){
      return 'default name Vika'
    }
  }
}

admin = new Proxy(admin, handler)

console.log(admin.name) //default name Vika
```


#programming/web/frontend/js