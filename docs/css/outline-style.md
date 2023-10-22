---
description: Свойство outline-style устанавливает стиль внешней границы элемента
---

# outline-style

Свойство **`outline-style`** устанавливает стиль внешней границы элемента.

В отличие от линии, задаваемой через [`border`](border.md), линия через `outline` отображается вокруг элемента, не влияя на ширину блока или его положение.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/outline-style.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Интерфейс"

    <div class="col3" markdown="1">

    - [appearance](appearance.md)
    - [box-sizing](box-sizing.md)
    - [caret-color](caret-color.md)
    - [cursor](cursor.md)
    - [outline](outline.md)
    - [outline-width](outline-width.md)
    - **outline-style**
    - [outline-color](outline-color.md)
    - [outline-offset](outline-offset.md)
    - [resize](resize.md)
    - [text-overflow](text-overflow.md)
    - [user-select](user-select.md)

    </div>

## Синтаксис

```css
/* Keyword values */
outline-style: auto;
outline-style: none;
outline-style: dotted;
outline-style: dashed;
outline-style: solid;
outline-style: double;
outline-style: groove;
outline-style: ridge;
outline-style: inset;
outline-style: outset;

/* Global values */
outline-style: inherit;
outline-style: initial;
outline-style: unset;
```

## Значения

`none`

: Граница не отображается. Это значение перекрывает свойство [`outline-width`](outline-width.md), если оно присутствует.

`dotted`

: Линия состоящая из набора точек.

`dashed`

: Пунктирная линия, состоящая из серии коротких отрезков.

`solid`

: Сплошная линия.

`double`

: Двойная линия.

`groove`

: Создаёт эффект вдавленной рамки.

`ridge`

: Создаёт эффект рельефной границы.

`inset`

: Псевдотрёхмерная рамка, при которой правая и нижняя граница осветляется, а левая и верхняя линии затемняются.

`outset`

: Псевдотрёхмерная рамка, при которой левая и верхняя граница имеют более светлый оттенок, чем заданный цвет, а правая и нижняя линии затемняются.

Вид указанных стилей представлен на рис. 1.

![Рис. 1. Вид границы с разным значением стилей](border_style_10.png)

Значение по-умолчанию: `none`

Применяется ко всем элементам

## Спецификации

-   [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#outline-style)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/ui.html#propdef-outline-style)

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
        <title>outline-style</title>
        <style>
            .noborder a {
                outline-style: none; /* Убираем границу вокруг ссылок */
            }
        </style>
    </head>
    <body>
        <p>
            <a href="http://ya.ru">Яндекс</a>
            <a href="http://google.ru">Google</a>
        </p>

        <p class="noborder">
            <a href="http://ya.ru">Яндекс</a>
            <a href="http://google.ru">Google</a>
        </p>
    </body>
</html>
```
