---
description: Свойство image-rendering сообщает браузеру, каким алгоритмом интерполировать изображение при масштабировании его размеров или изменении масштаба в параметрах браузера
---

# image-rendering

Свойство **`image-rendering`** сообщает браузеру, каким алгоритмом интерполировать изображение при масштабировании его размеров или изменении масштаба в параметрах браузера.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/image-rendering.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения, фильтры, композиция"

    <div class="col3" markdown="1">

    - [image-orientation](image-orientation.md)
    - **image-rendering**
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
    - [filter](filter.md)

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
/* Keyword values */
image-rendering: auto;
image-rendering: crisp-edges;
image-rendering: pixelated;

/* Global values */
image-rendering: inherit;
image-rendering: initial;
image-rendering: unset;
```

## Значения

`auto`

: Браузер применяет встроенный в него алгоритм интерполяции, обычно применяется бикубический метод.

`crisp-edges`

: Цель алгоритма — быстрое отображение картинки, для чего применяется метод интерполяции по ближайшим точкам. Он не создаёт сглаживания вокруг линий и его можно рекомендовать в тех случаях, когда требуется сохранить первоначальный набор цветов и резкость краёв.

`pixelated`

: При увеличении размера картинки сохраняет контраст и контуры изображения, не допуская размытия цветов и контуров. При уменьшении размеров аналогичен `auto`.

### Примечание

-   Chrome вместо `crisp-edges` поддерживает значение `-webkit-optimize-contrast`.
-   Opera поддерживает значение `-o-crisp-edges`.
-   Firefox поддерживает значение `-moz-crisp-edges`.

Значение по-умолчанию:

```css
image-rendering: auto;
```

Применяется к изображениям, фоновым картинкам, [`<video>`](../html/video.md), [`<canvas>`](../html/canvas.md)

## Спецификации

-   [CSS Images Module Level 3](https://w3c.github.io/csswg-drafts/css-images/#the-image-rendering)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>image-rendering</title>
        <style>
            img {
                border: 1px solid #ccc;
            }
            .fast {
                image-rendering: pixelated;
            }
        </style>
    </head>
    <body>
        <p>
            <img
                src="image/russia.png"
                alt="Флаг России"
                width="200"
            />
            <img
                src="image/russia.png"
                alt="Флаг России"
                width="200"
                class="fast"
            />
        </p>
    </body>
</html>
```
