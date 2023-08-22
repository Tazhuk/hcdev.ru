---
description: Тег th (от англ. table heading — заголовок таблицы) предназначен для создания одной ячейки таблицы, которая обозначается как заголовочная
---

# &lt;th&gt;

Тег **`<th>`** _(от англ. **t**able **h**eading — заголовок таблицы)_ предназначен для создания одной ячейки таблицы, которая обозначается как заголовочная.

Текст в такой ячейке отображается браузером обычно жирным шрифтом и выравнивается по центру. Элемент `<th>` должен размещаться внутри контейнера [`<tr>`](tr.md), который в свою очередь располагается внутри [`<table>`](table.md).

## Демо

<iframe class="interactive is-tabbed-taller-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/th.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Таблицы"

    <div class="col4" markdown="1">

    - [caption](caption.md)
    - [col](col.md)
    - [colgroup](colgroup.md)
    - [table](table.md)
    - [tbody](tbody.md)
    - [td](td.md)
    - [tfoot](tfoot.md)
    - **th**
    - [thead](thead.md)
    - [tr](tr.md)

    </div>

## Синтаксис

```html
<table>
    <tr>
        <th>...</th>
    </tr>
</table>
```

Закрывающий тег не обязателен.

## Атрибуты

[`colspan`](#colspan)
: Объединяет горизонтальные ячейки.

[`headers`](#headers)
: Позволяет связать ячейки таблицы с заголовками в речевых браузерах.

[`rowspan`](#rowspan)
: Объединяет вертикальные ячейки.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### colspan

Устанавливает число ячеек, которые должны быть объединены по горизонтали. Этот атрибут имеет смысл для таблиц, состоящих из нескольких строк.

**Синтаксис**

```html
<th colspan="<число>">...</th>
```

**Значения**

Любое целое положительное число больше 1.

**Значение по умолчанию**

`1`

### headers

Позволяет связать ячейки таблицы с заголовками. Этот атрибут предназначен для повышения доступности таблицы пользователям речевых браузеров, в обычных браузерах результат применения атрибута `headers` не заметен.

Для связывания ячеек между собой, ячейке в `<th>` пишется атрибут `id`, а в другой ячейке — атрибут `headers` со значением, совпадающим со значением `id`.

**Синтаксис**

```html
<th id="<идентификатор>">...</th>
<th headers="<идентификатор>">...</th>
```

**Значения**

Один или несколько идентификаторов, разделённых между собой пробелом.

**Значение по умолчанию**

Нет.

### rowspan

Устанавливает число ячеек, которые должны быть объединены по вертикали. Этот атрибут имеет смысл для таблиц, состоящих из нескольких строк.

**Синтаксис**

```html
<th rowspan="<число>">...</th>
```

**Значения**

Любое целое положительное число больше 1.

**Значение по умолчанию**

`1`

## Значения ARIA role

-   `role=columnheader` для заголовочной ячейки в столбце
-   `role=rowheader` для заголовочной ячейки в строке

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/tables.html#the-th-element)
-   [HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-th-element)

## Описание и примеры

```html
<html>
    <head>
        <meta
            http-equiv="Content-Type"
            content="text/html; charset=utf-8"
        />
        <title>TH</title>
        <style type="text/css">
            table {
                border-collapse: collapse; /* Отображать двойные линии как одинарные */
            }
            th {
                background: #ccc; /* Цвет фона */
                text-align: left; /* Выравнивание по левому краю */
            }
            td,
            th {
                border: 1px solid #800; /* Параметры границы */
                padding: 4px; /* Поля в ячейках */
            }
        </style>
    </head>
    <body>
        <table width="100%" cellspacing="0" border="1">
            <tr>
                <th>Браузер</th>
                <th colspan="3">Internet Explorer</th>
                <th colspan="3">Opera</th>
                <th colspan="2">Firefox</th>
            </tr>
            <tr>
                <th>Версия</th>
                <td>5.5</td>
                <td>6.0</td>
                <td>7.0</td>
                <td>7.0</td>
                <td>8.0</td>
                <td>9.0</td>
                <td>1.0</td>
                <td>2.0</td>
            </tr>
            <tr>
                <th>Поддерживается</th>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
                <td>Да</td>
            </tr>
        </table>
    </body>
</html>
```

## Ссылки

-   Тег [`<th>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/th) <sup><small>MDN (рус.)</small></sup>
