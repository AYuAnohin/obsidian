Async await - это специальных синтаксис для работы с промисами. Всегда возвращает промис.(и await тоже возварщает всегда промис).

```js
asynh function getData(){
	return await fetch(https://api.data/getData)
}
```

#programming/web/frontend/js