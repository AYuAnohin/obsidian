Декоратор - это способ расширения возможностей функции путем ее обертки в другую.(используется в многих яп)

Декоратор функции - это функция которая принимает в аргументы функцию возможности которой надо расширить и возвращает другую функцию уже с расширенным функционалом.

```js
function checkArguments(fn){
  return (...args)=>{
    if(fn.length != args.length){
      throw new Error('too many arguments')
    } else {
      return fn(...args)
    }
  }
}

let multiply = function (a,b){
  return a * b
}

multiply = checkArguments(multiply)

console.log(multiply(4,5)) //20
console.log(multiply(4,5,6)) //error
```

#programming/web/frontend/js