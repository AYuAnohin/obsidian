Map - это структура данных([[Структуры данных]]), использующая как и [[Object js]] ключ/значение. Но map позволяет использовать ключи любого типа.
```js
let map = new Map(); //создание map
map.set(1, 'yes it\'s working') //установка значения
map.get(1) //получение значения - yes it's working
map.has(1) //true - проверка
console.log(map.size) //1
new Map(Object.entries(obj)) //из обычного объекта в map
Object.fromEntries(map) //из map в обычный объект
map.delete(1) //удаляет элемент по ключу
map.clear() //очищает коллекцию от всех элементов
//или так
let map = new Map([[1,    'num1']]);
```

Для перебора использовать универсальные методы для перебора структур данных. [[Перебор структур данных]] или forEach.

Также есть WeakMap он необходимой для более грамотной работой с памятью.

#programming/web/frontend/js