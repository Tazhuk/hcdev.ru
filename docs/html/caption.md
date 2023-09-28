---
description: Тег caption (от англ. caption - заголовок, подпись) предназначен для создания заголовка к таблице и может размещаться только внутри контейнера table
---

# &lt;caption&gt;

Тег **`<caption>`** _(от англ. **caption** - заголовок, подпись)_ предназначен для создания заголовка к таблице и может размещаться только внутри контейнера [`<table>`](table.md), причём сразу после открывающего тега.

Такой заголовок представляет собой текст, по умолчанию отображаемый перед таблицей и описывающий её содержание.

## Демо

<iframe class="interactive is-tabbed-taller-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/caption.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Таблицы"

    <div class="col4" markdown="1">

    - **caption**
    - [col](col.md)
    - [colgroup](colgroup.md)
    - [table](table.md)
    - [tbody](tbody.md)
    - [td](td.md)
    - [tfoot](tfoot.md)
    - [th](th.md)
    - [thead](thead.md)
    - [tr](tr.md)

    </div>

## Синтаксис

```html
<table>
    <caption>
        Текст
    </caption>
    <tr>
        <td>...</td>
    </tr>
</table>
```

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/tables.html#the-caption-element)
-   [HTML5](http://www.w3.org/TR/html5/tabular-data.html#the-caption-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/tables.html#h-11.2.2)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>CAPTION</title>
        <style>
            table {
                width: 100%;
            }
            td {
                border: 1px solid #000;
                padding: 4px;
            }
        </style>
    </head>
    <body>
        <table>
            <caption>
                Таблица 3.2. Демонстрация катаболических
                процессов организма
            </caption>
            <tr>
                <th></th>
                <th>Чебурашка</th>
                <th>Крокодил Гена</th>
                <th>Шапокляк</th>
            </tr>
            <tr>
                <td>Съел, кг</td>
                <td>5</td>
                <td>2</td>
                <td>1</td>
            </tr>
            <tr>
                <td>Выпил, л</td>
                <td>6</td>
                <td>8</td>
                <td>2</td>
            </tr>
            <tr>
                <td>Смог, раз</td>
                <td>5</td>
                <td>5</td>
                <td>1</td>
            </tr>
        </table>
    </body>
</html>
```

## Ссылки

-   Тег [`<caption>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/caption) <sup><small>MDN (рус.)</small></sup>
