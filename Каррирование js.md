Каррирование - продвинутая техника для работы с функциями. Позволяющая принимать аргументы как f(a)(b)(c).
```js
function sum(a){
  return function (b){
    return a + b
  }
}

console.log(sum(5)(4))
```

#programming/web/frontend/js