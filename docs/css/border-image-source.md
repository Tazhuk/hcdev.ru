---
description: Свойство border-image-source определяет изображение вместо стиля границы
---

# border-image-source

Свойство **`border-image-source`** определяет изображение вместо стиля границы.

Если это свойство установлено в `none`, вместо него используется стиль, определяемый [`border-style`](border-style.md).

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/border-image-source.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

Свойство `border-image-slice` используется для разделения исходного изображения на области, которые затем динамически применяются к конечному изображению границы.

??? info "Фон"

    <div class="col3" markdown="1">

    - [border](border.md)
    - [border-bottom](border-bottom.md)
    - [border-bottom-color](border-bottom-color.md)
    - [border-bottom-left-radius](border-bottom-left-radius.md)
    - [border-bottom-right-radius](border-bottom-right-radius.md)
    - [border-bottom-style](border-bottom-style.md)
    - [border-bottom-width](border-bottom-width.md)
    - [border-collapse](border-collapse.md)
    - [border-color](border-color.md)
    - [border-image](border-image.md)
    - [border-image-outset](border-image-outset.md)
    - [border-image-repeat](border-image-repeat.md)
    - [border-image-slice](border-image-slice.md)
    - **border-image-source**
    - [border-image-width](border-image-width.md)
    - [border-left](border-left.md)
    - [border-left-color](border-left-color.md)
    - [border-left-style](border-left-style.md)
    - [border-left-width](border-left-width.md)
    - [border-radius](border-radius.md)
    - [border-right](border-right.md)
    - [border-right-color](border-right-color.md)
    - [border-right-style](border-right-style.md)
    - [border-right-width](border-right-width.md)
    - [border-style](border-style.md)
    - [border-top](border-top.md)
    - [border-top-color](border-top-color.md)
    - [border-top-left-radius](border-top-left-radius.md)
    - [border-top-right-radius](border-top-right-radius.md)
    - [border-top-style](border-top-style.md)
    - [border-top-width](border-top-width.md)
    - [border-width](border-width.md)
    - [box-shadow](box-shadow.md)

    </div>

## Синтаксис

```css
/* Keyword value */
border-image-source: none;

/* <image> values */
border-image-source: url(image.jpg);
border-image-source: linear-gradient(to top, red, yellow);

/* Global values */
border-image-source: inherit;
border-image-source: initial;
border-image-source: revert;
border-image-source: revert-layer;
border-image-source: unset;
```

## Значения

`none`

: Изображение границы не используется. Вместо этого отображается внешний вид, определенный бордюром.

`<image>`

: Ссылка на изображение для границы.

Значение по-умолчанию:

```css
border-image-source: none;
```

## Спецификации

-   [CSS Backgrounds and Borders Module Level 3](https://w3c.github.io/csswg-drafts/css-backgrounds/#the-border-image-source)

## Поддержка браузерами

<p class="ciu_embed" data-feature="border-image" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=border-image">Can I Use border-image?</a> Data on support for the border-image feature across the major browsers from caniuse.com.
</p>
