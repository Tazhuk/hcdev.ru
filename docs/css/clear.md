---
description: Свойство clear устанавливает, с какой стороны элемента запрещено его обтекание другими элементами
---

# clear

Свойство **`clear`** устанавливает, с какой стороны элемента запрещено его обтекание другими элементами.

Если задано обтекание элемента с помощью свойства [`float`](float.md), то `clear` отменяет его действие для указанных сторон.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/clear.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Позиционирование"

    <div class="col3" markdown="1">

    - [bottom](bottom.md)
    - **clear**
    - [display](display.md)
    - [float](float.md)
    - [left](left.md)
    - [position](position.md)
    - [right](right.md)
    - [top](top.md)
    - [z-index](z-index.md)

    </div>

## Синтаксис

```css
/* Keyword values */
clear: none;
clear: left;
clear: right;
clear: both;
clear: inline-start;
clear: inline-end;

/* Global values */
clear: inherit;
clear: initial;
clear: revert;
clear: revert-layer;
clear: unset;
```

## Значения

`none`

: Отменяет действие свойства `clear`, при этом обтекание элемента происходит, как задано с помощью свойства [`float`](float.md) или других настроек.

`both`

: Отменяет обтекание элемента одновременно с правого и левого края. Это значение рекомендуется устанавливать, когда требуется снять обтекание элемента, но неизвестно точно с какой стороны.

`left`

: Отменяет обтекание с левого края элемента. При этом все другие элементы на этой стороне будут опущены вниз, и располагаться под текущим элементом.

`right`

: Отменяет обтекание с правой стороны элемента.

Значение по-умолчанию:

```css
clear: none;
```

Применяется к блочным элементам

## Спецификации

-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#flow-control)
-   [CSS Level 1](http://www.w3.org/TR/CSS1/#clear)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>clear</title>
        <style>
            .pull-left {
                float: left; /* Обтекание блока по правому краю */
                padding-right: 10px;
            }
            .clearfix {
                clear: both;
            }
        </style>
    </head>
    <body>
        <div class="pull-left">
            <img src="image/figure.jpg" alt="" />
        </div>
        <div class="clearfix"></div>
        <p>
            Бихевиоризм, как бы это ни казалось
            парадоксальным, просветляет сублимированный
            стимул, так, например, Ричард Бендлер для
            построения эффективных состояний использовал
            изменение субмодальностей.
        </p>
    </body>
</html>
```
