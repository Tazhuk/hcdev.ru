---
description: Свойство table-layout определяет, как браузер должен вычислять ширину ячеек таблицы, основываясь на её содержимом
---

# table-layout

Свойство **`table-layout`** определяет, как браузер должен вычислять ширину ячеек таблицы, основываясь на её содержимом.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/table-layout.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - [empty-cells](empty-cells.md)
    - **table-layout**
    - [vertical-align](vertical-align.md)

    </div>

## Синтаксис

```css
/* Keyword values */
table-layout: auto;
table-layout: fixed;

/* Global values */
table-layout: inherit;
table-layout: initial;
table-layout: revert;
table-layout: revert-layer;
table-layout: unset;
```

## Значения

`auto`

: Браузер загружает всю таблицу, анализирует её для определения размеров ячеек и только после этого отображает.

`fixed`

: Ширина колонок в этом случае определяется либо с помощью тега [`<col>`](../html/col.md), либо вычисляется на основе первой строки. Если данные о форматировании первой строки таблицы по каким-либо причинам получить невозможно, в этом случае таблица делится на колонки равной ширины. При использовании этого значения, содержимое, которое не помещается в ячейку указанной ширины, будет «обрезано» либо наложено поверх ячейки. Это зависит от используемого браузера, но в любом случае ширина ячейки меняться не будет. Для корректной работы этого значения обязательно должна быть задана ширина таблицы.

Значение по-умолчанию: `auto`

Применяется к тегу [`<table>`](../html/table.md) или к элементу, у которого значение [`display`](display.md) установлено как `table` или `inline-table`.

## Спецификации

-   [Cascading Style Sheets Level 2 Revision 2 (CSS 2.2) Specification](https://w3c.github.io/csswg-drafts/css2/#width-layout)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/tables.html#width-layout)

## Поддержка браузерами

<p class="ciu_embed" data-feature="mdn-css__properties__table-layout" data-periods="future_1,current,past_1,past_2" data-accessible-colours="false"></p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>table-layout</title>
        <style>
            table {
                table-layout: fixed; /* Фиксированная ширина ячеек */
                width: 100%; /* Ширина таблицы */
            }
            .col1 {
                width: 160px;
            }
            .coln {
                width: 60px;
            }
        </style>
    </head>
    <body>
        <table border="1">
            <col class="col1" />
            <col span="9" class="coln" />
            <tr>
                <td></td>
                <td>2012</td>
                <td>2013</td>
                <td>2014</td>
                <td>2015</td>
                <td>2016</td>
                <td>2017</td>
                <td>2018</td>
                <td>2019</td>
                <td>2020</td>
            </tr>
            <tr>
                <td>Нефть</td>
                <td>5</td>
                <td>7</td>
                <td>2</td>
                <td>8</td>
                <td>3</td>
                <td>34</td>
                <td>62</td>
                <td>74</td>
                <td>57</td>
            </tr>
            <tr>
                <td>Золото</td>
                <td>3</td>
                <td>6</td>
                <td>4</td>
                <td>6</td>
                <td>4</td>
                <td>69</td>
                <td>72</td>
                <td>56</td>
                <td>47</td>
            </tr>
            <tr>
                <td>Дерево</td>
                <td>5</td>
                <td>8</td>
                <td>3</td>
                <td>4</td>
                <td>7</td>
                <td>73</td>
                <td>79</td>
                <td>34</td>
                <td>86</td>
            </tr>
        </table>
    </body>
</html>
```
