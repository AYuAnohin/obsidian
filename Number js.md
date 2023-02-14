Числа в js это один из простых типов данных.

```js
1e5 // короткая запись 100000
```

Округление
```js
Math.floor(3.2)
Math.ceil(3.2)
Math.round(4.7)
Math.trunc(3.2)
12.36..toFixed(1) //12.4
```

В js есть проблема с дробями, связанная с потерей точности, из-за того что дробь в двоичной системе стоновится бесконечной. Решается проблема простым отбрасыванием хвоста.

Проверки числа
```js
IsNaN(value)
isFinite(value) //не NaN/infinity
```

Отбросить конец
```js
parseInt(12px) //12
parseFloat(12.2px) //12.2
```

Объект Math который содержит множество функций.

#programming/web/frontend/js