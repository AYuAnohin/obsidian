apply позволяет вызвать функции в контексте необходимого нам объекта([[call]]), только аргументы пробрасываюься в виде массива.
```js
Math.max.apply(null, [1,26,2,66,2])//66
```

#programming/web/frontend/js