---
metaTitle: Число в JavaScript
metaDescription: Разбираемся как работают числа в JavaScript
author: Дмитрий Нечаев
title: Число в JavaScript
preview: Учимся пользоваться числами в JavaScript. Разбираем примеры использования
---

В JavaScript числа используются для представления числовых значений. Это может быть как целое число, так и число с плавающей точкой. В этой статье мы рассмотрим основы работы с числовым типом данных в JavaScript, включая его свойства, методы и примеры использования.

### Создание чисел

Для создания чисел в JavaScript используется простой синтаксис. Числа могут быть записаны как целые числа, так и числа с плавающей точкой.

```jsx
const integer = 42; // Целое число
const float = 3.14; // Число с плавающей точкой

```

### Арифметические операции

JavaScript поддерживает все основные арифметические операции: сложение, вычитание, умножение и деление. Эти операции могут применяться как к целым числам, так и к числам с плавающей точкой.

```jsx
const sum = 10 + 5; // Сложение
const difference = 10 - 5; // Вычитание
const product = 10 * 5; // Умножение
const quotient = 10 / 5; // Деление

```

### Свойства числа

У чисел в JavaScript есть ряд свойств, которые можно использовать для получения информации о числе. Например, свойство `.MAX_VALUE` возвращает максимально возможное число в JavaScript.

```jsx
console.log(Number.MAX_VALUE); // Выведет: 1.7976931348623157e+308

```

### Методы числа

В JavaScript также существует набор методов, которые можно использовать для работы с числами. Например, метод `.toFixed()` позволяет округлить число до указанного количества десятичных знаков.

```jsx
const number = 3.14159;
console.log(number.toFixed(2)); // Выведет: 3.14

```

### Преобразование строки в число

JavaScript также позволяет преобразовывать строки в числа с помощью функции `parseInt()` или `parseFloat()`.

```jsx
const str = "42";
const num = parseInt(str); // Преобразует строку в целое число
console.log(num); // Выведет: 42

```

### Проверка на число

Чтобы проверить, является ли значение числом, можно использовать функцию `isNaN()`. Она возвращает `true`, если значение не является числом, и `false`, если является.

```jsx
console.log(isNaN(42)); // Выведет: false
console.log(isNaN("abc")); // Выведет: true

```

### Заключение

Числа являются важным типом данных в JavaScript и используются повсеместно в различных сценариях программирования. Они позволяют выполнять арифметические операции, хранить числовые данные и выполнять различные вычисления. Понимание основ работы с числовым типом данных в JavaScript поможет вам эффективно использовать числа в ваших скриптах и разрабатывать более функциональные приложения.