---
metaTitle: Псевдокласс not в CSS. Исключаем элементы с определённым признаком
metaDescription: Псевдокласс not в CSS. Исключаем элементы с определённым признаком
author: Дмитрий Нечаев
title: Псевдокласс not в CSS. Полное руководство с примерами
preview: Псевдокласс not в CSS используется для исключения из выборки селектора элементов, которые соответствуют указанному критерию.
---

Псевдокласс `:not` в CSS используется для исключения из выборки селектора элементов, которые соответствуют указанному критерию. Это мощный инструмент, позволяющий создать более точные и гибкие правила стилизации. В этой статье мы подробно рассмотрим псевдокласс `:not`, его применение и приведём примеры использования для различных ситуаций.

## Что такое псевдокласс `:not`?

Псевдокласс `:not` исключает из выборки селектора элементы, которые соответствуют указанному селектору. Это позволяет избежать применения стилей к определённым элементам, сохраняя при этом стилизацию для остальных элементов.

Пример базового использования `:not`:

```css
selector:not(selector) {
  /* Стили для элементов, которые не соответствуют указанному селектору */
}

```

Пример использования псевдокласса `:not` для исключения элементов с классом `excluded`:

```css
div:not(.excluded) {
  background-color: lightblue;
}

```

В этом примере все `<div>`, которые не имеют класса `excluded`, будут с фоном светло-голубого цвета.

## Примеры использования псевдокласса `:not`

### Основные примеры

### Исключение элемента по классу

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    p:not(.highlight) {
      color: black; /* Применение чёрного цвета к абзацам без класса .highlight */
    }

    p.highlight {
      color: red; /* Применение красного цвета к абзацам с классом .highlight */
    }
  </style>
  <title>Исключение элемента по классу</title>
</head>
<body>
  <p>Это обычный абзац.</p>
  <p class="highlight">Это выделенный абзац.</p>
  <p>Ещё один обычный абзац.</p>
</body>
</html>

```

В этом примере все абзацы, кроме тех, которые имеют класс `highlight`, будут чёрного цвета.

### Исключение элемента по тегу

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    *:not(p) {
      margin: 0; /* Убираем отступы у всех элементов, кроме <p> */
    }
  </style>
  <title>Исключение элемента по тегу</title>
</head>
<body>
  <h1>Заголовок 1</h1>
  <p>Абзац текста.</p>
  <div>Див с текстом.</div>
</body>
</html>

```

В этом примере отступы будут убраны у всех элементов, кроме `<p>`.

### Исключение элемента по атрибуту

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    a:not([target="_blank"]) {
      text-decoration: none; /* Убираем подчеркивание у всех ссылок, кроме тех, которые открываются в новой вкладке */
    }
  </style>
  <title>Исключение элемента по атрибуту</title>
</head>
<body>
  <a href="<https://example.com>" target="_blank">Ссылка с открытием в новой вкладке</a>
  <a href="<https://example.com>">Обычная ссылка</a>
</body>
</html>

```

В этом примере подчеркивание будет убрано у всех ссылок, кроме тех, которые открываются в новой вкладке.

### Сложные примеры

### Комбинирование с другими псевдоклассами

Псевдокласс `:not` можно комбинировать с другими псевдоклассами для создания сложных селекторов.

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    li:not(:first-child) {
      background-color: lightgray; /* Применение фона к элементам списка, кроме первого */
    }
  </style>
  <title>Комбинирование с другими псевдоклассами</title>
</head>
<body>
  <ul>
    <li>Первый элемент</li>
    <li>Второй элемент</li>
    <li>Третий элемент</li>
  </ul>
</body>
</html>

```

В этом примере фон будет применён ко всем элементам списка, кроме первого.

### Исключение нескольких селекторов

Псевдокласс `:not` поддерживает исключение нескольких селекторов с помощью группировки.

Пример:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    p:not(.highlight):not(.special) {
      color: black; /* Применение чёрного цвета к абзацам, не имеющим классов .highlight и .special */
    }

    p.highlight {
      color: red; /* Применение красного цвета к абзацам с классом .highlight */
    }

    p.special {
      color: blue; /* Применение синего цвета к абзацам с классом .special */
    }
  </style>
  <title>Исключение нескольких селекторов</title>
</head>
<body>
  <p>Это обычный абзац.</p>
  <p class="highlight">Это выделенный абзац.</p>
  <p class="special">Это специальный абзац.</p>
  <p>Ещё один обычный абзац.</p>
</body>
</html>

```

В этом примере все абзацы, кроме тех, которые имеют классы `highlight` и `special`, будут чёрного цвета.

### Использование в реальных проектах

### Стилизация меню

Использование псевдокласса `:not` для стилизации пунктов меню, исключая первый и последний элементы:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    nav ul li:not(:first-child):not(:last-child) {
      background-color: lightblue; /* Применение фона к элементам списка, кроме первого и последнего */
      margin: 5px 0;
    }

    nav ul li {
      padding: 10px;
    }
  </style>
  <title>Стилизация меню</title>
</head>
<body>
  <nav>
    <ul>
      <li>Главная</li>
      <li>О нас</li>
      <li>Услуги</li>
      <li>Контакты</li>
    </ul>
  </nav>
</body>
</html>

```

В этом примере фон будет применён ко всем пунктам меню, кроме первого и последнего.

### Стилизация форм

Использование псевдокласса `:not` для стилизации полей формы, исключая поля с определёнными атрибутами:

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    input:not([type="submit"]):not([type="reset"]) {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 3px;
    }
  </style>
  <title>Стилизация форм</title>
</head>
<body>
  <form>
    <label for="name">Имя:</label>
    <input type="text" id="name" name="name">
    <br><br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    <br><br>
    <input type="submit" value="Отправить">
    <input type="reset" value="Сбросить">
  </form>
</body>
</html>

```

В этом примере ширина, отступы и границы будут применены ко всем полям ввода, кроме кнопок отправки и сброса.

## Заключение

Псевдокласс `:not` в CSS предоставляет мощный способ для исключения из выборки селектора элементов, которые соответствуют определённому критерию. Это позволяет создавать более точные и гибкие правила

стилизации, улучшая внешний вид и функциональность веб-страниц. Понимание различных способов использования псевдокласса `:not`, а также его комбинирование с другими селекторами и псевдоклассами, помогает разработчикам создавать адаптивные и поддерживаемые стили. Экспериментируйте с различными подходами и находите оптимальные решения для ваших проектов.