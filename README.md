# JS_Objects

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*AIXCysLdHdwKAyNMTucaTw.gif" width="full" height="400px">
</div>

# 🌟 JavaScript Objects
*JavaScript Objects — это одна из ключевых частей языка. Они позволяют хранить данные в формате "ключ-значение" и являются основой для работы с более сложными структурами, такими как классы или JSON.*

# 🤔 Что такое объект?
*В JavaScript объект — это коллекция свойств, где каждое свойство связано с ключом (имя) и значением.*

Пример объекта:
```js
const person = {
    name: "Alice",
    age: 25,
    city: "New York"
};
```
*📌 Здесь person — это объект с тремя свойствами:*

- name — значение "Alice"
- age — значение 25
- city — значение "New York"

# 🚀 Основные операции с объектами

<div align="center">
  <img src="https://www.linuxlinks.com/wp-content/uploads/2023/04/fx.gif" width="600px" height="400px">
</div>

### Доступ к свойствам
*Точечная нотация:*
```js
console.log(person.name); // "Alice"
```

*Квадратные скобки:*
```js
console.log(person["city"]); // "New York"
```

### Добавление свойств
```js
person.country = "USA";
console.log(person);
// { name: "Alice", age: 25, city: "New York", country: "USA" }
```

### Удаление свойств
```js
delete person.age;
console.log(person);
// { name: "Alice", city: "New York", country: "USA" }
```

### Проверка существования свойства
```js
console.log("name" in person); // true
console.log("age" in person); // false
```

# ✨ Перебор свойств объекта*

<div align="center">
  <img src="https://fireship.io/courses/javascript/img/js-object-props.png" width="600px" height="400px">
</div>

*for...in*
Позволяет перебрать все свойства объекта:
```js
for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
// name: Alice
// city: New York
// country: USA
```

#### Методы Object

*a) Object.keys(obj)*
Возвращает массив ключей:
```js
console.log(Object.keys(person)); 
// ["name", "city", "country"]
```

*b) Object.values(obj)*
Возвращает массив значений:
```js
console.log(Object.values(person)); 
// ["Alice", "New York", "USA"]
```

*c) Object.entries(obj)*
Возвращает массив пар [ключ, значение]:
```js
console.log(Object.entries(person));
// [["name", "Alice"], ["city", "New York"], ["country", "USA"]]
```

# 🧰 Вложенные объекты
*Объекты могут содержать другие объекты.*
```js
const student = {
    name: "Bob",
    grades: {
        math: 90,
        science: 85
    }
};

console.log(student.grades.math); // 90
```

# ⚡ Методы объектов
*Методы — это функции, которые являются свойствами объекта.*
```js
const calculator = {
    add(a, b) {
        return a + b;
    },
    subtract(a, b) {
        return a - b;
    }
};

console.log(calculator.add(5, 3)); // 8
console.log(calculator.subtract(5, 3)); // 2
```

# 🛠️ Работа с прототипами
*Каждый объект в JavaScript имеет прототип, который можно использовать для наследования свойств и методов.*

Пример:
```js
const animal = {
    eat() {
        console.log("Eating...");
    }
};

const dog = Object.create(animal);
dog.bark = function() {
    console.log("Woof!");
};

dog.eat(); // "Eating..."
dog.bark(); // "Woof!"
```

# 🔥 Современные подходы к работе с объектами

### Деструктуризация
*Позволяет извлекать свойства объекта в переменные.*
```js
const { name, city } = person;
console.log(name); // "Alice"
console.log(city); // "New York"
```

### Расширение объектов
```js
const newPerson = { ...person, age: 30 };
console.log(newPerson);
// { name: "Alice", city: "New York", country: "USA", age: 30 }
```

Заключение
*JavaScript Objects* — это универсальный инструмент для хранения данных и работы с ними. Понимание объектов открывает двери к пониманию JSON, классов, наследования и многого другого.

---

<div align="center">
  <img src="https://a.d-cd.net/fGkj61MC91njUbKjZUahzEm1-IA-960.jpg" width="600px" height="300px">
</div>

---
