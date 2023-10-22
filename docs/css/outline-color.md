---
description: Свойство outline-color указывает цвет внешней границы элемента
---

# outline-color

Свойство **`outline-color`** указывает цвет внешней границы элемента.

В отличие от линии, задаваемой через [`border`](border.md), линия через свойство `outline` отображается вокруг элемента, не влияя на ширину блока или его положение.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/outline-color.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Интерфейс"

    <div class="col3" markdown="1">

    - [appearance](appearance.md)
    - [box-sizing](box-sizing.md)
    - [caret-color](caret-color.md)
    - [cursor](cursor.md)
    - [outline](outline.md)
    - [outline-width](outline-width.md)
    - [outline-style](outline-style.md)
    - **outline-color**
    - [outline-offset](outline-offset.md)
    - [resize](resize.md)
    - [text-overflow](text-overflow.md)
    - [user-select](user-select.md)

    </div>

## Синтаксис

```css
/* <color> values */
outline-color: #f92525;
outline-color: rgb(30, 222, 121);
outline-color: blue;

/* Keyword value */
outline-color: invert;

/* Global values */
outline-color: inherit;
outline-color: initial;
outline-color: unset;
```

## Значения

`invert`

: Автоматически задаёт цвет линии, исходя из фона под ней для достижения максимального контраста. В CSS 2.1 браузеру разрешается игнорировать значение `invert` и вместо него использовать цвет линии заданный свойством [`color`](color.md).

`<цвет>`

: Задаёт цвет линии в любом допустимом для CSS формате.

### Примечание

Chrome, Android и Safari не поддерживают значение `invert`.

Значение по-умолчанию: `invert`

Применяется ко всем элементам

## Спецификации

-   [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#outline-color)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/ui.html#propdef-outline-color)

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
        <title>outline-color</title>
        <style>
            .block {
                outline-style: dashed; /* Пунктирная граница */
                outline-color: #be8b5e; /* Цвет границы */
                padding: 10px; /* Поля вокруг текста */
                background: #eedac8; /* Цвет фона */
            }
        </style>
    </head>
    <body>
        <div class="block">
            Воображение, на первый взгляд, начинает
            конструктивный классицизм.
        </div>
    </body>
</html>
```
