# &lt;tbody&gt;

Тег **`<tbody>`** _(от англ. **t**able **body** — тело таблицы)_ предназначен для хранения одной или нескольких строк таблицы.

Это позволяет создавать структурные блоки, к которым можно применять единое оформление через стили, а также управлять их видом через скрипты.

Допускается применять несколько элементов `<tbody>` внутри контейнера [`<table>`](table.md). Доступны и другие виды группировок строк — [`<tfoot>`](tfoot.md) и [`<thead>`](thead.md), ни один из них не должен перекрываться с элементом `<tbody>`.

## Демо

<iframe class="interactive is-tabbed-taller-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/tbody.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Таблицы"

    <div class="col4" markdown="1">

    - [caption](caption.md)
    - [col](col.md)
    - [colgroup](colgroup.md)
    - [table](table.md)
    - **tbody**
    - [td](td.md)
    - [tfoot](tfoot.md)
    - [th](th.md)
    - [thead](thead.md)
    - [tr](tr.md)

    </div>

## Синтаксис

```html
<table>
    <thead>
        ...
    </thead>
    <tfoot>
        ...
    </tfoot>
    <tbody>
        <tr>
            <td>...</td>
        </tr>
    </tbody>
</table>
```

Закрывающий тег не обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/tables.html#the-tbody-element)
-   [HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-tbody-element)

## Описание и примеры

```html
<html>
    <head>
        <meta
            http-equiv="Content-Type"
            content="text/html; charset=utf-8"
        />
        <title>TBODY</title>
    </head>
    <body>
        <table width="600" border="1">
            <tbody align="right">
                <tr>
                    <td>Ячейка 1</td>
                    <td>Ячейка 2</td>
                </tr>
            </tbody>
        </table>
    </body>
</html>
```

## Ссылки

-   Тег [`<tbody>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/tbody) <sup><small>MDN (рус.)</small></sup>
