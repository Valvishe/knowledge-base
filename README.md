# База знаний PurpleSchool

PurpleSchool Knowledge Base - единая база знаний по стеку JavaScript для frontend, backend и мобильной разработки, а так же DevOps.
База знаний полностью открыта, поддерживается и наполняется силами школы и сообщества. Её основная задача – давать актуальные знания по технологиям и служить справочной информацией для изучения материала.

Сайт проекта: https://purpleschool.ru/knowledge-base

### Как устроена база знаний?

В данном репозитории хранятся статьи, материалы и изображения. Один раз в неделю все статьи, которые находятся в `master` ветке выкладываются на сайт.

### Как помочь и внести свой вклад?

Вы со своей стороны можете помочь нам в её развитии и наполнении. Для этого вам достаточно сделать всего несколько простых шагов:

- Сделать fork этого репозитория.
- Выберите тему для статьи, которую вы хотите добавить.
- Найдите нужную папку для статьи. Для этого следуйте следующей структуре:
  - /typescript - верхнеуровневая тема для статьи. Этот уровень не изменяется, вы просто должны выбрать его.
  - /typescript/types/ - раздел под вашу статью. Если он ещё не существует, то вы можете его создать используя инструкцию "Создание раздела"
  - /typescript/types/unknown-how-to-use - папка статьи. Если вы хотите создать новую статью, то на уровне к примеру /typescript/types вам необходимо будет создать новую папку и index.md по инструкции "Создание статьи"
- Написать статьи и заполнить все теги по инструкциям ниже.
- Сделать Pull Request.
  В течение недели модератор ознакомится с вашей статьёй, предложит правки или просто сделает merge.

### Создание раздела

Если вы не видите подходящий раздел для добавления материала, то вы можете его создать. Для этого создайте папку в верхнеуровневой теме и внутри добавьте файл index.md со следующим содержамнием:

```markdown
---
metaTitle: Типы TypeScript
metaDescription: Описание для типов
title: Типы
---

Типы
```

- metaTitle - краткое описание раздела, которое будет отображаться в заголовке вкладки.
- metaDescription - описание раздела для поисковиков
- title - название раздела для отображения в списке
  Ниже добавляется краткое описание раздела, рассказывающее что в нём будет.

### Создание статьи

В разделе создайте папке с названием, где можно использовать только латинские буквы, цифры и дефис. Пример: how-to-use-unknown.
Внутри этой папки создайте файл index.md, где и будет располагаться ваша статья. Если нужно, вы можете создать внутри подпапку images для размещения изображений.

```markdown
---
metaTitle: Как правильно использовать тип Unknown
metaDescription: Разбираемся как использовать тип Unknown правльно
author: Василий Майоров
title: Как правильно использовать тип Unknown
preview: Использование типа any в TypeScript нежелательно. В наиболее строгом режиме (оно настраивается) использование any невозможно, что значительно повышает типобезопасность кода. С другой стороны, существует немало ситуаций, когда тип неизвестен, но работа с ним должна быть типобезопасна.
---

Сама статья
```

- metaTitle - краткое описание статьи, которое будет отображаться в заголовке вкладки.
- metaDescription - описание статьи для поисковиков
- author - ваше имя и фамилия
- title - название статьи для отображения в списке
- preview - краткое описание статьи для отображения в списке, не более 100-200 символов
  Ниже располагается статья. Можно использовать все возможности markdown. При добавлении блока кода важно указывать язык: typescript, javascript, css, html и так далее для корректной подсветки синтаксиса.