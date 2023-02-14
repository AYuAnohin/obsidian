callback - это функция которая пробрасывается в аргумент при вызове другой функции, чаще всего анонимная(или всегда, потому что я не вижу смысла пробрасывать не анонимную функцию, я же ее могу так вызвать).
```js
function first(callback){
	setTimeout(()=>{
		console.log(1)
		callback() 
	}, 2000)
}
first(()=>{
	console.log(5)
}) // это анонимная функция callback
```


#programming/web/frontend/js