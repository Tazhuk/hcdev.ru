---
description: Тег tfoot (от англ. table foot — подвал таблицы) предназначен для хранения одной или нескольких строк, которые представлены внизу таблицы
---

# &lt;tfoot&gt;

Тег **`<tfoot>`** _(от англ. **t**able **foot** — подвал таблицы)_ предназначен для хранения одной или нескольких строк, которые представлены внизу таблицы.

Хотя `<tfoot>` в исходном коде должен быть определён до элемента [`<tbody>`](tbody.md), браузеры отображают его в самом низу таблицы.

В пределах таблицы разрешается использовать только один элемент `<tfoot>`.

## Демо

<iframe class="interactive is-tabbed-taller-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/tfoot.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Таблицы"

    <div class="col4" markdown="1">

    - [caption](caption.md)
    - [col](col.md)
    - [colgroup](colgroup.md)
    - [table](table.md)
    - [tbody](tbody.md)
    - [td](td.md)
    - **tfoot**
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
        <tr>
            <td>...</td>
        </tr>
    </tfoot>
    <tbody>
        ...
    </tbody>
</table>
```

Закрывающий тег не обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/tables.html#the-tfoot-element)
-   [HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-tfoot-element)

## Описание и примеры

```html
<html>
    <head>
        <meta
            http-equiv="Content-Type"
            content="text/html; charset=utf-8"
        />
        <title>TFOOT</title>
    </head>
    <body>
        <table width="600">
            <tfoot align="center" style="background: #ffc">
                <tr>
                    <td>Ячейка 1, расположенная в TFOOT</td>
                    <td>Ячейка 2, расположенная в TFOOT</td>
                </tr>
            </tfoot>
            <tbody align="right" style="background: silver">
                <tr>
                    <td>Ячейка 3, расположенная в TBODY</td>
                    <td>Ячейка 4, расположенная в TBODY</td>
                </tr>
            </tbody>
        </table>
    </body>
</html>
```

## Ссылки

-   Тег [`<tfoot>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/tfoot) <sup><small>MDN (рус.)</small></sup>
