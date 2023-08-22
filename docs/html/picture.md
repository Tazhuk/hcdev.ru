---
description: Тег picture (от англ. picture — картина, изображение) представляет собой контейнер для хранения нескольких элементов source, которые поддерживают элемент img
---

# &lt;picture&gt;

Тег **`<picture>`** _(от англ. **picture** — картина, изображение)_ представляет собой контейнер для хранения нескольких элементов [`<source>`](source.md), которые поддерживают элемент [`<img>`](img.md).

Это позволяет указывать разные изображения с учётом размера экрана, плотности пикселей, формата изображения и других параметров. Вот несколько областей применения `<picture>`:

-   для экранов ретина можно показывать картинку большего размера;
-   выводить рисунки разного размера для мобильных и настольных устройств;
-   отображать изображения разных пропорций, учитывающих ориентацию устройства;
-   выводить изображение в векторном формате SVG, а для браузеров, его не поддерживающих, показывать PNG.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/picture.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения и мультимедиа"

    <div class="col4" markdown="1">

    - [area](area.md)
    - [audio](audio.md)
    - [img](img.md)
    - [figcaption](figcaption.md)
    - [figure](figure.md)
    - [map](map.md)
    - [track](track.md)
    - [video](video.md)
    - [embed](embed.md)
    - [iframe](iframe.md)
    - [object](object.md)
    - [param](param.md)
    - **picture**
    - [source](source.md)

    </div>

## Поддержка браузерами

<p class="ciu_embed" data-feature="picture" data-periods="future_1,current,past_1,past_2">
<a href="http://caniuse.com/#feat=picture">Can I Use picture?</a> Data on support for the picture feature across the major browsers from caniuse.com.
</p>

Полифилы для включения поддержки:

-   [`<picture>` polyfill](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills#picture-and-img-srcset)

## Синтаксис

```html
<picture>
    <source />
    <img />
</picture>
```

Внутри `<picture>` содержится ноль или несколько элементов [`<source>`](source.md), которые идут перед одним элементом [`<img>`](img.md).

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/embedded-content.html#the-picture-element)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>picture</title>
    </head>
    <body>
        <picture>
            <source srcset="image/html5-logo.svg" />
            <img
                src="image/html5-logo.png"
                width="256"
                height="256"
                alt="HTML5"
            />
        </picture>
    </body>
</html>
```

## Ссылки

-   Тег [`<picture>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/picture) <sup><small>MDN (рус.)</small></sup>
