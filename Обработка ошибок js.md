Обработать ошибку можно с помощью try/catch/finally
```js
try {
	console.log('comlit')
  	throw new SyntaxError("можно прокинуть свою ошибку")
} catch(err) {
	console.dir(err + ' hm')
} finally {
	console.log('just')
}
//complit
//SyntaxError: можно прокинуть свою ошибку hm
//just
```
В catch мы получаем объект error, он содержит
1. Имя ошибки - ReferenceError
2. Текстовое сообщение ошибки - gg is not defined hm
3. Стек - последовательность вложенных вызовов которые привели к ошибке

Блок catch должен обрабатывать только те ошибки которые мы хотим обработать, а те ошибки которые мы не знаем нужно прокидывать через throw дальше.


#programming/web/frontend/js