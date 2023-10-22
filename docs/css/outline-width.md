---
description: Свойство outline-width определяет толщину внешней границы элемента
---

# outline-width

Свойство **`outline-width`** определяет толщину внешней границы элемента.

В отличие от свойства [`border-width`](border-width.md), для `outline-width` нельзя задать границу для каждой стороны элемента индивидуально.

Чтобы `outline-width` работал, необходимо установить у свойства [`outline-style`](outline-style.md) любое значение кроме `none`.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/outline-width.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Интерфейс"

    <div class="col3" markdown="1">

    - [appearance](appearance.md)
    - [box-sizing](box-sizing.md)
    - [caret-color](caret-color.md)
    - [cursor](cursor.md)
    - [outline](outline.md)
    - **outline-width**
    - [outline-style](outline-style.md)
    - [outline-color](outline-color.md)
    - [outline-offset](outline-offset.md)
    - [resize](resize.md)
    - [text-overflow](text-overflow.md)
    - [user-select](user-select.md)

    </div>

## Синтаксис

```css
/* Keyword values */
outline-width: thin;
outline-width: medium;
outline-width: thick;

/* <length> values */
outline-width: 1px;
outline-width: 0.1em;

/* Global values */
outline-width: inherit;
outline-width: initial;
outline-width: revert;
outline-width: revert-layer;
outline-width: unset;
```

## Значения

`thin`

: Тонкая линия. Значение в пикселах может изменяться в зависимости от браузера, но обычно составляет 1 пиксел.

`medium`

: Линия средней толщины (3 пиксела).

`thick`

: Линия большой толщины (6 пикселов).

`<размер>`

: Для точной установки толщины можно использовать любые единицы размера принятые в CSS.

Значение по-умолчанию: `medium`

Применяется ко всем элементам

## Спецификации

-   [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#outline-width)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/ui.html#propdef-outline-width)

## Поддержка браузерами

<p class="ciu_embed" data-feature="outline" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=outline">Can I Use outline?</a> Data on support for the outline feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>outline-width</title>
        <style>
            .block {
                outline-style: dotted; /* Пунктирная внешняя граница */
                outline-width: 3px; /* Толщина внешней границы */
                padding: 10px; /* Поля вокруг текста */
                border: 3px dotted #000; /* Параметры рамки */
            }
        </style>
    </head>
    <body>
        <div class="block">
            Кондуктометрия мягко передает электронный способ
            получения независимо от последствий
            проникновения метилкарбиола внутрь.
        </div>
    </body>
</html>
```
