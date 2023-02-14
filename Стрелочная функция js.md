Стрелочные функции(лямда функция) имеют более короткий синтаксис и не имеюют собственного this, их this берется у родителя.

```js
let group = {
  title: "Our Group",
  students: ["John", "Pete", "Alice"],

  showList() {
    this.students.forEach(
      student => alert(this.title + ': ' + student)
    );
  }
};

group.showList();
```

Если бы я прокинул обычную функцию, this в этом случае был бы равен undefined/

#programming/web/frontend/js