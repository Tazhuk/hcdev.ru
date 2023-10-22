---
description: Свойство max-height устанавливает максимальную высоту элемента
---

# max-height

Свойство **`max-height`** устанавливает максимальную высоту элемента.

Значение высоты элемента будет вычисляться в зависимости от значений установленных свойств [`height`](height.md), `max-height` и [`min-height`](min-height.md).

Если значение высоты (`height`) больше значения `max-height`, то высота элемента принимается равной значению `max-height`.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/max-height.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Блоки"

    <div class="col3" markdown="1">

    - [height](height.md)
    - [width](width.md)
    - **max-height**
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
    - [overflow-x](overflow-x.md)
    - [overflow-y](overflow-y.md)
    - [visibility](visibility.md)

    </div>

## Синтаксис

```css
/* <length> value */
max-height: 3.5em;

/* <percentage> value */
max-height: 75%;

/* Keyword values */
max-height: none;
max-height: max-content;
max-height: min-content;
max-height: fit-content;
max-height: fill-available;

/* Global values */
max-height: inherit;
max-height: initial;
max-height: unset;
```

## Значения

В качестве значений принимаются пиксели (px), проценты (%) и другие единицы измерения, принятые в CSS. Отрицательные значения не допускаются.

`none`

: Отменяет действие этого свойства.

Значение по-умолчанию:

```css
max-height: none;
```

Применяется ко всем элементам, кроме строчных и таблиц

## Спецификации

-   [CSS Intrinsic & Extrinsic Sizing Module Level 3](http://dev.w3.org/csswg/css3-sizing/#width-height-keywords)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visudet.html#min-max-heights)

## Поддержка браузерами

<p class="ciu_embed" data-feature="minmaxwh" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=minmaxwh">Can I Use minmaxwh?</a> Data on support for the minmaxwh feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>max-height</title>
        <style>
            .block {
                overflow: auto; /* Полоса прокрутки при необходимости */
                padding: 10px; /* Поля вокруг текста */
                max-height: 80px; /* Максимальная высота */
                background: #ffe; /* Цвет фона */
                border: 1px solid #cb2027; /* Параметры рамки */
            }
            .block p {
                margin: 2px auto; /* Отступы в абзаце */
            }
        </style>
    </head>
    <body>
        <div class="block">
            <p>
                Блокирование элемента не позволяет вообще
                производить с ним каких-либо действий, в том
                числе выделять содержимое текстового поля,
                изменять его или активизировать.
                Заблокированное поле помечается обычно серым
                цветом
            </p>
            <p>
                Некоторые браузеры позволяют выделять и
                копировать содержимое заблокированного
                текстового поля, но все остальные действия
                недоступны.
            </p>
        </div>
    </body>
</html>
```
