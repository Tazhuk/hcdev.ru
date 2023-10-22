---
description: Тег td (от англ. table data — данные таблицы) предназначен для создания одной ячейки таблицы
---

# &lt;td&gt;

Тег **`<td>`** _(от англ. **t**able **d**ata — данные таблицы)_ предназначен для создания одной ячейки таблицы.

Элемент `<td>` должен размещаться внутри контейнера [`<tr>`](tr.md), который в свою очередь располагается внутри [`<table>`](table.md).

## Демо

<iframe class="interactive is-tabbed-taller-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/td.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Таблицы"

    <div class="col4" markdown="1">

    - [caption](caption.md)
    - [col](col.md)
    - [colgroup](colgroup.md)
    - [table](table.md)
    - [tbody](tbody.md)
    - **td**
    - [tfoot](tfoot.md)
    - [th](th.md)
    - [thead](thead.md)
    - [tr](tr.md)

    </div>

## Синтаксис

```html
<table>
    <tr>
        <td>...</td>
    </tr>
</table>
```

Закрывающий тег не обязателен.

## Атрибуты

`colspan`

: Объединяет горизонтальные ячейки.

`headers`

: Позволяет связать ячейки с заголовком.

`rowspan`

: Объединяет вертикальные ячейки.

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### colspan

Устанавливает число ячеек, которые должны быть объединены по горизонтали. Этот атрибут имеет смысл для таблиц, состоящих из нескольких строк.

**Синтаксис**

```html
<td colspan="<число>">...</td>
```

**Значения**

Любое целое положительное число. Значение 0 распространяет ячейку на всю родительскую группу колонок, объединённую элементом [`<colgroup>`](colgroup.md). Значения выше 1000 считаются неправильными и устанавливаются в 1.

**Значение по умолчанию**

`1`

### headers

Позволяет связать ячейки таблицы с заголовками. Этот атрибут предназначен для повышения доступности таблицы пользователям речевых браузеров, в обычных браузерах результат применения атрибута `headers` не заметен.

Для связывания ячеек между собой одной ячейке в элементе `<td>` или [`<th>`](th.md) задаётся атрибут `id`, а второй ячейке — атрибут `headers` со значением, совпадающим со значением `id`.

**Синтаксис**

```html
<td id="<идентификатор>">...</td>
<td headers="<идентификатор>">...</td>
```

**Значения**

Один или несколько идентификаторов, разделенных между собой пробелом.

**Значение по умолчанию**

Нет.

### rowspan

Устанавливает число ячеек, которые должны быть объединены по вертикали. Этот атрибут имеет смысл для таблиц, состоящих из нескольких строк.

**Синтаксис**

```html
<td rowspan="<число>">...</td>
```

**Значения**

Любое целое положительное число. Если значение установлено как 0, то ячейки объединяются до конца раздела таблицы ([`<thead>`](thead.md), [`<tbody>`](tbody.md) или [`<tfoot>`](tfoot.md)) или самой таблицы. Максимально допустимое значение равно 65534.

**Значение по умолчанию**

`1`

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/tables.html#the-td-element)
-   [HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-td-element)

## Описание и примеры

```html
<html>
    <head>
        <meta
            http-equiv="Content-Type"
            content="text/html; charset=utf-8"
        />
        <title>TD</title>
    </head>
    <body>
        <table border="1" cellpadding="7" cellspacing="0">
            <tr>
                <td
                    colspan="2"
                    bgcolor="#D3EDF6"
                    align="center"
                >
                    Ячейка 1
                </td>
            </tr>
            <tr>
                <td valign="top" align="center">
                    Ячейка 2
                </td>
                <td width="98%" valign="top">Ячейка 3</td>
            </tr>
        </table>
    </body>
</html>
```

## Ссылки

-   Тег [`<td>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/td) <sup><small>MDN (рус.)</small></sup>
