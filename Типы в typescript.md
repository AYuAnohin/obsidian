Пример присвоения типа(Часто типы определяются автоматически):
```ts
let boolFalse: boolean = false;
let multitypeVar: string | number = 'String'
```

Какие типы бывают:
1. numbers
3. strings
5. structures
6. boolean
8. array
```ts
let strings: string[] = ['Hello', 'World', '!']
```
Сосздать массив с помощью [[Дженерики ts]]
```ts
let numbers: Array<number> = [1, 2, 3, 4, 5]
```
10. tuple - объявить массив с известным количеством аргументов.
```ts
let x:[string, number] = ['age', 18]
```
8. enum
9. any
10. void - не возращает ничего
```ts
function warnUser(): void {
    alert("This is my warning message");
}
```
11. Assertion
Type assertion это превращения одного типа в друго(тип any передаются в функции, у которой приему аргументу указан тип).
```ts
let str: any = 'Текстовая переменная'
let strLength = (str as string).length
```
Тоже самое
```ts
let str: any = 'Текстовая переменная'
let strLength = (<string>str).length
```