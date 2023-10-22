---
description: Свойство overflow-x управляет отображением содержания блочного элемента по горизонтали, если контент целиком не помещается и выходит за область справа или слева от блока
---

# overflow-x

Свойство **`overflow-x`** управляет отображением содержания блочного элемента по горизонтали, если контент целиком не помещается и выходит за область справа или слева от блока.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/overflow-x.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Блоки"

    <div class="col3" markdown="1">

    - [height](height.md)
    - [width](width.md)
    - [max-height](max-height.md)
    - [max-width](max-width.md)
    - [min-height](min-height.md)
    - [min-width](min-width.md)

    </div>

    <div class="col3" markdown="1">

    - [margin](margin.md)
    - [margin-bottom](margin-bottom.md)
    - [margin-left](margin-left.md)
    - [margin-right](margin-right.md)
    - [margin-top](margin-top.md)
    - [margin-trim](margin-trim.md)

    </div>

    <div class="col3" markdown="1">

    - [padding](padding.md)
    - [padding-bottom](padding-bottom.md)
    - [padding-left](padding-left.md)
    - [padding-right](padding-right.md)
    - [padding-top](padding-top.md)

    </div>

    <div class="col3" markdown="1">

    - [overflow](overflow.md)
    - **overflow-x**
    - [overflow-y](overflow-y.md)
    - [visibility](visibility.md)

    </div>

## Синтаксис

```css
/* Keyword values */
overflow-x: visible;
overflow-x: hidden;
overflow-x: clip;
overflow-x: scroll;
overflow-x: auto;

/* Global values */
overflow-x: inherit;
overflow-x: initial;
overflow-x: revert;
overflow-x: revert-layer;
overflow-x: unset;
```

## Значения

`visible`

: Отображается всё содержание элемента, даже за пределами установленной ширины.

`hidden`

: Отображается только область внутри элемента, остальное будет скрыто.

`scroll`

: Всегда добавляется горизонтальная полоса прокрутки.

`auto`

: Горизонтальная полоса прокрутки добавляется только при необходимости.

Значение по-умолчанию: `visible`

Применяется к блочным элементам

## Спецификации

-   [CSS Basic Box Model](http://dev.w3.org/csswg/css3-box/#overflow-x)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>overflow-x</title>
        <style>
            .layer {
                overflow-x: scroll; /* Добавляем полосу прокрутки */
                width: 300px; /* Ширина блока */
                height: 150px; /* Высота блока */
                padding: 5px; /* Поля вокруг текста */
                border: solid 1px black; /* Параметры рамки */
                white-space: nowrap; /* Запрещаем перенос строк */
            }
        </style>
    </head>
    <body>
        <div class="layer">
            <h2>Гетерогенный голубой гель</h2>
            <p>
                Кондуктометрия мягко передает электронный
                способ получения независимо от последствий
                проникновения метилкарбиола внутрь.
            </p>
        </div>
    </body>
</html>
```
