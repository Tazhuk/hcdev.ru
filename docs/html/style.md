---
description: Тег style (от англ. style — стиль) применяется для определения стилей элементов веб-страницы
---

# &lt;style&gt;

Тег **`<style>`** _(от англ. **style** — стиль)_ применяется для определения стилей элементов веб-страницы.

Элемент `<style>` необходимо использовать внутри контейнера [`<head>`](head.md). Можно задавать несколько `<style>`.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/style.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Метаданные документа"

    <div class="col4" markdown="1">

    - [base](base.md)
    - [link](link.md)
    - [meta](meta.md)
    - **style**
    - [title](title.md)

    </div>

## Синтаксис

```html
<head>
    <style>
        ...;
    </style>
</head>
```

Закрывающий тег обязателен.

## Атрибуты

[`media`](#media)
: Определяет устройство вывода, для работы с которым предназначена таблица стилей.

[`type`](#type)
: Сообщает браузеру, какой синтаксис использовать, чтобы правильно интерпретировать стили.

### media

Устанавливает устройство вывода, для которого предназначена таблица стилей. Для каждого устройства можно определить свой собственный стиль, который бы учитывал специфику устройства и подгонял под него вид веб-страницы.

**Синтаксис**

```html
<style media="all | print | screen | speech">
    ...;
</style>
```

**Значения**

`all`
: Все устройства.

`print`
: Печатающее устройство вроде принтера.

`screen`
: Экран монитора.

`speech`
: Речевые синтезаторы, а также программы для воспроизведения текста вслух. Сюда же входят речевые браузеры.

Можно устанавливать сразу несколько значений, перечисляя их через запятую.

**Значение по умолчанию**

-   `screen`

### type

Сообщает браузеру, какой синтаксис использовать, чтобы правильно интерпретировать таблицу стилей. Как правило, браузеры корректно работают со стилями и при отсутствии этого атрибута, он необходим для некоторых старых браузеров, которые могут не распознать содержимое контейнера `<style>`.

В HTML4 этот атрибут является обязательным, в HTML5 его можно опустить.

**Синтаксис**

```html
<style type="text/css">
    ...;
</style>
```

**Значения**

В качестве значения используется MIME-тип — `text/css`.

**Значение по умолчанию**

-   `text/css`

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/document-metadata.html#the-style-element)
-   [HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-style-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/present/styles.html#h-14.2.3)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>STYLE, атрибут media</title>
        <style media="screen">
            .window {
                background: #333;
                border: 1px solid red;
                font-size: 0.9em;
                color: #fc0;
                padding: 10px;
            }
        </style>
        <style media="print">
            .window {
                border: 1px solid black;
                font-family: Arial;
                font-size: 0.9em;
                color: black;
                padding: 10px;
            }
        </style>
    </head>
    <body>
        <div class="window">
            Ветеринарное свидетельство входит экскурсионный
            эфемероид, но особой популярностью пользуются
            заведения подобного рода, сосредоточенные в
            районе Центральной площади и железнодорожного
            вокзала.
        </div>
    </body>
</html>
```

## Ссылки

-   Тег [`<style>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/style) <sup><small>MDN (рус.)</small></sup>
