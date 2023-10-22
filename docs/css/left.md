---
description: Свойство left для позиционированного элемента определяет расстояние от левого края родительского элемента, не включая отступ, поле и ширину рамки, до левого края дочернего элемента
---

# left

Свойство **`left`** для позиционированного элемента определяет расстояние от левого края родительского элемента, не включая отступ, поле и ширину рамки, до левого края дочернего элемента.

Отсчёт координат зависит от значения свойства [`position`](position.md). Если оно равно `absolute`, в качестве родителя выступает окно браузера и положение элемента определяется от его левого края (рис. 1).

![Рис. 1. Значение свойства left относительно окна браузера](css_left_1.png)

В случае значения `relative`, `left` отсчитывается от левого края исходного положения элемента (рис. 2).

![Рис. 2. Значение свойства left относительно исходного положения](css_left_2.png)

Если для родительского элемента задано `position: relative`, то абсолютное позиционирование дочерних элементов определяет их положение от левого края родителя.

![Рис. 3. Значение свойства left относительно родителя](css_left_3.png)

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/left.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Позиционирование"

    <div class="col3" markdown="1">

    - [bottom](bottom.md)
    - [clear](clear.md)
    - [display](display.md)
    - [float](float.md)
    - **left**
    - [position](position.md)
    - [right](right.md)
    - [top](top.md)
    - [z-index](z-index.md)

    </div>

## Синтаксис

```css
/* <length> values */
left: 3px;
left: 2.4em;

/* <percentage>s of the width of the containing block */
left: 10%;

/* Keyword value */
left: auto;

/* Global values */
left: inherit;
left: initial;
left: unset;
```

## Значения

В качестве значений принимаются любые единицы длины, принятые в CSS — например, пиксели (px), дюймы (in), пункты (pt) и др. Значение свойства `left` может быть и отрицательным, в этом случае возможны наложения разных элементов друг на друга. При задании значения в процентах, положение элемента вычисляется в зависимости от ширины родительского элемента.

`auto`

: Не изменяет положение элемента.

Значение по-умолчанию:

```css
left: auto;
```

Применяется ко всем элементам

## Спецификации

-   [CSS Positioned Layout Module Level 3](https://w3c.github.io/csswg-drafts/css-position/#insets)
-   [CSS Transitions](http://dev.w3.org/csswg/css-transitions/#animatable-css)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#propdef-left)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>left</title>
        <style>
            .layer1 {
                position: absolute; /* Абсолютное позиционирование */
                left: 20px; /* Положение от левого края */
                background: #fc3; /* Цвет фона */
                margin: 7px; /* Отступы вокруг элемента */
            }
            .layer2 {
                position: relative; /* Относительное позиционирование */
                left: -12px; /* Положение от левого края */
                top: 13px; /* Положение от верхнего края */
                border: 1px solid black; /* Параметры рамки */
                padding: 5px; /* Поля вокруг текста */
                margin: 7px; /* Отступы вокруг элемента */
            }
        </style>
    </head>
    <body>
        <div class="layer1">
            <div class="layer2">
                Бином Ньютона традиционно упорядочивает
                абсолютно сходящийся ряд, в итоге приходим к
                логическому противоречию.
            </div>
        </div>
    </body>
</html>
```
