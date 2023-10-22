---
description: Свойство overflow управляет отображением содержания блочного элемента, если оно целиком не помещается и выходит за область заданных размеров
---

# overflow

Свойство **`overflow`** управляет отображением содержания блочного элемента, если оно целиком не помещается и выходит за область заданных размеров.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/overflow.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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

    - **overflow**
    - [overflow-x](overflow-x.md)
    - [overflow-y](overflow-y.md)
    - [visibility](visibility.md)

    </div>

## Синтаксис

```css
/* Keyword values */
overflow: visible;
overflow: hidden;
overflow: clip;
overflow: scroll;
overflow: auto;
overflow: hidden visible;

/* Global values */
overflow: inherit;
overflow: initial;
overflow: revert;
overflow: revert-layer;
overflow: unset;
```

## Значения

`visible`

: Отображается всё содержимое элемента, даже за пределами установленной высоты и ширины.

`hidden`

: Отображается только область внутри элемента, остальное будет скрыто.

`scroll`

: Всегда добавляются полосы прокрутки.

`auto`

: Полосы прокрутки добавляются только при необходимости.

Значение по-умолчанию: `visible`

Применяется к блочным элементам

## Спецификации

-   [CSS Basic Box Model](https://drafts.csswg.org/css-box-3/#overflow-intro)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visufx.html#overflow)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>overflow</title>
        <style>
            .layer {
                overflow: scroll; /* Добавляем полосы прокрутки */
                width: 300px; /* Ширина блока */
                height: 150px; /* Высота блока */
                padding: 5px; /* Поля вокруг текста */
                border: solid 1px black; /* Параметры рамки */
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
