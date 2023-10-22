---
description: Свойство transform трансформирует элемент, в частности, позволяет его масштабировать, вращать, сдвигать, наклонять, а также комбинировать виды трансформаций
---

# transform

Свойство **`transform`** трансформирует элемент, в частности, позволяет его масштабировать, вращать, сдвигать, наклонять, а также комбинировать виды трансформаций.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/transform.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Трансформации"

    <div class="col3" markdown="1">

    - [backface-visibility](backface-visibility.md)
    - [perspective](perspective.md)
    - [perspective-origin](perspective-origin.md)
    - [rotate](rotate.md)
    - [scale](scale.md)
    - **transform**
    - [transform-box](transform-box.md)
    - [transform-origin](transform-origin.md)
    - [transform-style](transform-style.md)

    </div>

## Синтаксис

```css
/* Keyword values */
transform: none;

/* Function values */
transform: matrix(1, 2, 3, 4, 5, 6);
transform: translate(12px, 50%);
transform: translateX(2em);
transform: translateY(3in);
transform: scale(2, 0.5);
transform: scaleX(2);
transform: scaleY(0.5);
transform: rotate(0.5turn);
transform: skew(30deg, 20deg);
transform: skewX(30deg);
transform: skewY(1.07rad);
transform: matrix3d(
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    8,
    9,
    10,
    11,
    12,
    13,
    14,
    15,
    16
);
transform: translate3d(12px, 50%, 3em);
transform: translateZ(2px);
transform: scale3d(2.5, 1.2, 0.3);
transform: scaleZ(0.3);
transform: rotate3d(1, 2, 3, 10deg);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: perspective(17px);

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);

/* Global values */
transform: inherit;
transform: initial;
transform: revert;
transform: revert-layer;
transform: unset;
```

## Значения

`<функция>`

: Функция трансформации.

`none`

: Отменяет действие трансформации.

## Функции трансформации

### `matrix()`

Задаёт двумерную матрицу преобразований.

### `matrix3d()`

Задаёт трёхмерную матрицу преобразований.

### `rotate()`

Поворачивает элемент в двумерном пространстве на заданный угол относительно точки трансформации, задаваемой свойством [`transform-origin`](transform-origin.md).

### `rotate3d()`

Поворачивает элемент в трёхмерном пространстве.

### `rotateX()`

Поворачивает элемент на заданный угол относительно оси X.

### `rotateY()`

Поворачивает элемент на заданный угол относительно оси Y.

### `rotateZ()`

Поворачивает элемента на заданный угол относительно оси Z.

### `scale()`

Масштабирует элемент по горизонтали и вертикали. Значение больше 1 увеличивает масштаб элемента, меньше 1 — уменьшает масштаб.

### `scale3d()`

Масштабирует элемент в трёхмерном пространстве.

### `scaleX()`

Масштабирует элемент по горизонтали.

### `scaleY()`

Масштабирует элемент по вертикали.

### `scaleZ()`

Масштабирует элемент по оси Z.

### `skew()`

Наклоняет элемент на заданный угол по вертикали и горизонтали.

### `skewX()`

Наклоняет элемент на заданный угол по вертикали.

### `skewY()`

Наклоняет элемент на заданный угол по горизонтали.

### `translate()`

Сдвигает элемент на заданное значение по горизонтали и вертикали.

### `translate3d()`

Сдвигает элемент на заданное значение в трёхмерном пространстве.

### `translateX()`

Сдвигает элемент по горизонтали на указанное значение. Положительное значение сдвигает вправо, отрицательное влево.

### `translateY()`

Сдвигает элемент по вертикали на указанное значение. Положительное значение сдвигает вниз, отрицательное вверх.

### `translateZ()`

Сдвигает элемент по оси Z на указанное значение. Положительное значение сдвигает назад, отрицательное вперёд.

### `perspective()`

Задаёт перспективу.

### Примечание

-   Internet Explorer 9 поддерживает свойство `-ms-transform`.
-   Chrome до версии 36 и Android до версии 4 поддерживают свойство `-webkit-transform`.
-   Safari поддерживает свойство `-webkit-transform`.
-   Opera до версии 12.10 и с версии 15 до 23 поддерживает свойство `-o-transform`.
-   Firefox до версии 16 поддерживает свойство `-moz-transform`.

Значение по-умолчанию: `none`

Применяется к трансформируемым элементам

## Спецификации

-   [CSS Transforms Module Level 2](https://w3c.github.io/csswg-drafts/css-transforms-2/#transform-functions)
-   [CSS Transforms Module Level 1](https://w3c.github.io/csswg-drafts/css-transforms/#transform-property)

## Поддержка браузерами

CSS Transform 2D:

<p class="ciu_embed" data-feature="transforms2d" data-periods="future_1,current,past_1,past_2"></p>

CSS Transform 3D:

<p class="ciu_embed" data-feature="transforms3d" data-periods="future_1,current,past_1,past_2"></p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>transform</title>
        <style>
            .turn:hover {
                transform: rotate(15deg);
            }
        </style>
    </head>
    <body>
        <p>
            <img
                src="image/igels.png"
                alt="Ёжик"
                class="turn"
            />
            <img
                src="image/igels.png"
                alt="Ёжик"
                class="turn"
            />
        </p>
    </body>
</html>
```
