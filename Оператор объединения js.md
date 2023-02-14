Оператор объединения(??), возварщает значение если это не null/undefined, если оба числа null/undefined, он возвращает null/undefined
Пример
```js
let a = 5
let b = 6

console.log(a ?? b) //5
console.log(false ?? b) //false
console.log(null ?? b) //6
```

#programming/web/frontend/js