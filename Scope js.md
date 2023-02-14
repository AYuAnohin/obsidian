Область видимости в js - важная концепция, определяющая доступность переменных.

Каждая функция при вызове имеет область видимости и контекст([[Context js]]) в котором вызывается.

Область видимости создаются каждый раз когда используется конструкция "{}"(функции, условия, циклы) и всегда иммеет доступ к наружным областям видимости.

```js
let a = 8
{
	let a = 5
  	console.log(a) //5
}
console.log(a) //8
```

Есть 3 вида области видимости:
1. Глобальная
2. Локальная
3. Лексическая

Глобальной областью видимости называют самую внешнюю область видимости, которая предостовляет объекты document, window как глобальные переменные.

Локальная область видимости это то что находится в {...}

Лексическая(статическая) область видимости посложнее
```js
let value = 2;

function showValue() {
 console.log("Value from showValue: " + value); // 2
}

function wrapper() {
 let value = 3;
 console.log("Value from wrapper: " + value); // 3

 showValue();
}
wrapper();
```

При компиляции js, компилятор лексически анализирует код. Он разбивает код на значимые участки, которые называются лексемами. То есть лексическая область видимости это область видимости, которая определенна во время разбора на лексемы. То есть по итогу лексической областью видимости называют именно лексическое местополжение этой области в коде.

Лексическое окружение.([[Lexical Environment]])


Есть еще динамическая область видимости, но она не используется в js.

#programming/web/frontend/js