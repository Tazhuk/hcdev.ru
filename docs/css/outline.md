---
description: Универсальное свойство outline, одновременно устанавливающее цвет, стиль и толщину внешней границы на всех четырёх сторонах элемента
---

# outline

Универсальное свойство **`outline`**, одновременно устанавливающее цвет, стиль и толщину внешней границы на всех четырёх сторонах элемента.

В отличие от линии, задаваемой через [`border`](border.md), свойство `outline` не влияет на положение блока и его ширину. Также нельзя задать параметры линии на отдельных сторонах элемента, `outline` применяется сразу ко всем четырём сторонам.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/outline.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Интерфейс"

    <div class="col3" markdown="1">

    - [appearance](appearance.md)
    - [box-sizing](box-sizing.md)
    - [caret-color](caret-color.md)
    - [cursor](cursor.md)
    - **outline**
    - [outline-width](outline-width.md)
    - [outline-style](outline-style.md)
    - [outline-color](outline-color.md)
    - [outline-offset](outline-offset.md)
    - [resize](resize.md)
    - [text-overflow](text-overflow.md)
    - [user-select](user-select.md)

    </div>

## Синтаксис

```css
/* style */
outline: solid;

/* color | style */
outline: #f66 dashed;

/* style | width */
outline: inset thick;

/* color | style | width */
outline: green solid 3px;

/* Global values */
outline: inherit;
outline: initial;
outline: revert;
outline: revert-layer;
outline: unset;
```

## Значения

`outline-color`

: Задаёт цвет линии в любом допустимом для CSS формате.

`outline-style`

: Стиль линии.

`outline-width`

: Толщина границы.

Значение по-умолчанию: Нет

Применяется ко всем элементам

## Спецификации

-   [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#outline)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/ui.html#propdef-outline)

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
        <title>outline</title>
        <style>
            .photo img {
                padding: 20px; /* Поля вокруг изображения */
                margin-right: 10px; /* Отступ справа */
                margin-bottom: 10px; /* Отступ снизу */
                outline: 1px solid #666; /* Параметры рамки */
                background: #f0f0f0; /* Цвет фона */
                float: left; /* Обтекание по правому краю */
            }
        </style>
    </head>
    <body>
        <div class="photo">
            <img
                src="image/girl.jpg"
                alt="Девочка с муфтой"
            />
            <img src="image/owl.jpg" alt="Сова" />
            <img
                src="image/boy.jpg"
                alt="Эвенкийский мальчик"
            />
        </div>
    </body>
</html>
```
