---
description: Свойство filter предназначено для применения художественных эффектов к элементам
---

# filter

Свойство **`filter`** предназначено для применения художественных эффектов к элементам.

Обычно используется для изображений, чтобы размыть их, увеличить контрастность, преобразовать в чёрно-белую картинку и др.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/filter.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения, фильтры, композиция"

    <div class="col3" markdown="1">

    - [image-orientation](image-orientation.md)
    - [image-rendering](image-rendering.md)
    - [image-resolution](image-resolution.md)
    - [object-fit](object-fit.md)
    - [object-position](object-position.md)

    </div>

    <div class="col3" markdown="1">

    - [linear-gradient()](linear-gradient.md)
    - [radial-gradient()](radial-gradient.md)
    - [repeating-linear-gradient()](repeating-linear-gradient.md)
    - [repeating-radial-gradient()](repeating-radial-gradient.md)
    - [conic-gradient()](conic-gradient.md)
    - [repeating-conic-gradient()](repeating-conic-gradient.md)
    - [url()](url.md)
    - [element()](element.md)
    - [image()](image.md)
    - [cross-fade()](cross-fade.md)

    </div>

    <div class="col3" markdown="1">

    - [backdrop-filter](backdrop-filter.md)
    - **filter**

    </div>

    <div class="col3" markdown="1">

    - [background-blend-mode](background-blend-mode.md)
    - [isolation](isolation.md)
    - [mix-blend-mode](mix-blend-mode.md)

    </div>

    <div class="col3" markdown="1">

    - [contain](contain.md)
    - [contain-intrinsic-block-size](contain-intrinsic-block-size.md)
    - [contain-intrinsic-height](contain-intrinsic-height.md)
    - [contain-intrinsic-inline-size](contain-intrinsic-inline-size.md)
    - [contain-intrinsic-size](contain-intrinsic-size.md)
    - [contain-intrinsic-width](contain-intrinsic-width.md)
    - [container](container.md)
    - [container-name](container-name.md)
    - [container-type](container-type.md)
    - [@container](container-at-rule.md)
    - [content-visibility](content-visibility.md)

    </div>

## Синтаксис

```css
/* URL to SVG filter */
filter: url('filters.svg#filter-id');

/* <filter-function> values */
filter: blur(5px);
filter: brightness(0.4);
filter: contrast(200%);
filter: drop-shadow(16px 16px 20px blue);
filter: grayscale(50%);
filter: hue-rotate(90deg);
filter: invert(75%);
filter: opacity(25%);
filter: saturate(30%);
filter: sepia(60%);

/* Multiple filters */
filter: contrast(175%) brightness(3%);

/* Global values */
filter: inherit;
filter: initial;
filter: unset;
```

## Значения

`<фильтр>`

: фильтр.

`none`

: Отменяет действие наложенных фильтров.

**Фильтр** — это функция, которая позволяет изменять вид изображения, применяя к нему разные эффекты, вроде контрастности, яркости, преобразования в чёрно-белую картинку и др.

### blur()

Функция **`blur()`** задаёт размытие по Гауссу изображений, фоновых картинок или текста. К элементу [`<body>`](../html/body.md) напрямую применить размытие нельзя, только к его потомкам.

**Синтаксис**

```
filter: blur(<размер>);
```

**Значения**

В качестве значения указывается радиус размытия, он пишется в любых доступных единицах размера CSS (к примеру: `5px`). Чем больше значение, тем сильнее будет размыто изображение.

Отрицательное значение не допускается. Пустое значение воспринимается как `0px`.

**Спецификация**

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#funcdef-blur)

### brightness()

Функция **`brightness()`** понижает или повышает яркость изображений или фоновых картинок.

**Синтаксис**

```
filter: brightness(<значение>);
```

**Значения**

Значение `100%` или `1` оставляет изображение исходным. Любые значения меньше `100%` (или меньше `1`) понижают яркость изображения. Таким образом, `0` даёт полностью чёрную картинку. Значения больше `100%` (или больше `1`) повышают яркость изображения.

Отрицательное значение не допускается. Пустое значение воспринимается как `1`.

**Спецификация**

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#funcdef-brightness)

### contrast()

Функция **`contrast()`** понижает или повышает контрастность изображений или фоновых картинок.

**Синтаксис**

```
filter: contrast(<значение>);
```

**Значения**

Значение `100%` или `1` оставляет изображение исходным. Любые значения меньше `100%` (или меньше `1`) понижают контрастность изображения. При этом `0` даёт однотонную серую картинку. Значения больше `100%` (или больше `1`) повышают контрастность изображения.

Отрицательное значение не допускается. Пустое значение воспринимается как `1`.

**Спецификация**

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#funcdef-contrast)

### drop-shadow()

Функция **`drop-shadow()`** добавляет тень к изображениям. В отличие от свойства [`box-shadow`](box-shadow.md) во внимание принимаются прозрачные участки в изображении и тень отбрасывается с их учётом.

**Синтаксис**

```
filter: drop-shadow(<сдвиг по x> <сдвиг по y> <радиус размытия> <цвет>);
```

**Значения**

`<сдвиг по x>`

: Смещение тени по горизонтали относительно картинки. Положительное значение этого параметра задаёт сдвиг тени вправо, отрицательное — влево. Обязательный параметр.

`<сдвиг по y>`

: Смещение тени по вертикали относительно картинки. Положительное значение задаёт сдвиг тени вниз, отрицательное — вверх. Обязательный параметр.

`<размытие>`

: Задаёт радиус размытия тени. Чем больше это значение, тем сильнее тень сглаживается, становится шире и светлее. Если этот параметр не задан, по умолчанию устанавливается равным `0`, тень при этом будет чёткой, а не размытой.

`<цвет>`

: Цвет тени в любом доступном CSS формате, по умолчанию тень чёрная. Необязательный параметр.

При пустом значении все параметры воспринимается как `0`. Цвет тени по умолчанию такой же, как значение свойства [`color`](color.md).

**Спецификация**

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#funcdef-drop-shadow)

### grayscale()

Функция **`grayscale()`** превращает изображение в чёрно-белое.

**Синтаксис**

```
filter: grayscale(<значение>);
```

**Значения**

Значение `100%` или `1` превращает изображение в чёрно-белое. Значение `0` оставляет изображение исходно цветным. Значения меньше `100%` (или меньше `1`) линейно меняют цветность картинки.

Отрицательное значение не допускается. Пустое значение воспринимается как `0`.

**Спецификация**

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#funcdef-grayscale)

### Примечания

-   Internet Explorer c версии 4 по 10 поддерживает другое нестандартное свойство `filter` с тем же именем, но другим синтаксисом.
-   Chrome до версии 53, Opera до версии 40 и Safari до версии 9.1 поддерживают свойство `-webkit-filter`.

Значение по-умолчанию:

```css
filter: none;
```

Применяется к: Ко всем элементам

## Спецификации

-   [Filter Effects Module Level 1](https://www.w3.org/TR/filter-effects/#propdef-filter)

## Поддержка браузерами

<p class="ciu_embed" data-feature="css-filters" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=css-filters">Can I Use css-filters?</a> Data on support for the css-filters feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>filter</title>
        <style>
            .bw {
                -webkit-filter: grayscale(100%);
                filter: grayscale(
                    100%
                ); /* Чёрно-белое изображение */
                transition: 1.5s; /* Плавный переход */
            }
            .bw:hover {
                -webkit-filter: none;
                filter: none; /* Убираем фильтр */
            }
        </style>
    </head>
    <body>
        <img src="image/aquaria2.jpg" alt="" class="bw" />
        <img src="image/aquaria3.jpg" alt="" class="bw" />
    </body>
</html>
```
