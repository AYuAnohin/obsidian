Promise - это специальный объект, который содержит состояние pending, но после вызова reject или resolve переходит в выполненное, он используется для отложенных или ассинхронный вычеслений(только не в этом примере)
```js
new Promise((resolve, reject)=>{
	resolve('success')
}).then((successText)=>{
	console.log(successText + ' success')
}).catch((errorText)=>{
	console.log(errorText + ' error')
}).finally(()=>{
	console.log('my work is done')
})
```

Ловить ошибку можно в catch или вторым аргументом в then

Потребители промиса(всегда ассинхронны)
1. then
2. catch
3. finally

C помощью then можно создать цепочку промисов.(для последовательного выполнения ассинхронных действий)

Promise API
Promise.all - дождаться выполнения всех промисов.
Promise.allSettled - приходит статус каждого промиса.
Promise.race - только самый быстрый промис.

Промисифакация - это преоброзование функции на колбеках в функцию на промисах.


#programming/web/frontend/js