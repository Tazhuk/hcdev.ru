---
direction: Свойство empty-cells задаёт отображение границ и фона в ячейке, если она пустая
---

# empty-cells

Свойство **`empty-cells`** задаёт отображение границ и фона в ячейке, если она пустая.

При одновременном добавлении к таблице свойства [`border-collapse`](border-collapse.md) со значением `collapse`, свойство `empty-cells` игнорируется.

Ячейка считается пустой в следующих случаях:

-   нет вообще никаких символов;
-   в ячейке содержится только перевод строки, символ табуляции или пробел;
-   значение [`visibility`](visibility.md) установлено как `hidden`.

Добавление неразрывного пробела `&nbsp`; воспринимается как видимое содержание, т. е. ячейка уже будет непустой.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/empty-cells.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Колонки и таблицы"

    <div class="col3" markdown="1">

    - [column-count](column-count.md)
    - [column-fill](column-fill.md)
    - [column-gap](column-gap.md)
    - [column-rule](column-rule.md)
    - [column-rule-color](column-rule-color.md)
    - [column-rule-style](column-rule-style.md)
    - [column-rule-width](column-rule-width.md)
    - [column-span](column-span.md)
    - [column-width](column-width.md)
    - [columns](columns.md)

    </div>

    <div class="col3" markdown="1">

    - [border-collapse](border-collapse.md)
    - [border-spacing](border-spacing.md)
    - [caption-side](caption-side.md)
    - **empty-cells**
    - [table-layout](table-layout.md)
    - [vertical-align](vertical-align.md)

    </div>

## Синтаксис

```css
/* Keyword values */
empty-cells: show;
empty-cells: hide;

/* Global values */
empty-cells: inherit;
empty-cells: initial;
empty-cells: unset;
```

## Значения

`show`

: Отображает границу вокруг ячейки и фон в ней.

`hide`

: Граница и фон в пустых ячейках не отображается. Если все ячейки в строке пустые, то строка прячется целиком.

Значение по-умолчанию:

```css
empty-cells: show;
```

Применяется к: К [`<td>`](../html/td.md), [`<th>`](../html/th.md) или к элементам, у которых [`display`](display.md)`: table-cell`

## Спецификации

-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/tables.html#empty-cells)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>empty-cells</title>
        <style>
            table {
                border: 4px double #399; /* Граница вокруг таблицы */
            }
            td {
                background: #fc0; /* Цвет фона */
                border: 1px solid #333; /* Граница вокруг ячеек */
                empty-cells: hide; /* Прячем пустые ячейки */
                padding: 5px; /* Поля в ячейках */
            }
        </style>
    </head>
    <body>
        <table width="100%">
            <tr>
                <td>Леонардо</td>
                <td>5</td>
                <td>8</td>
            </tr>
            <tr>
                <td>Рафаэль</td>
                <td></td>
                <td>11</td>
            </tr>
            <tr>
                <td>Микеланджело</td>
                <td>24</td>
                <td></td>
            </tr>
            <tr>
                <td>Донателло</td>
                <td></td>
                <td>13</td>
            </tr>
        </table>
    </body>
</html>
```
