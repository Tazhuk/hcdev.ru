---
description: Свойство page-break-inside разрешает или запрещает разрыв страницы внутри элемента при печати
---

# page-break-inside

!!!warning "Предупреждение"

    Это свойство было заменено свойством [`break-inside`](break-inside.md).

Свойство **`page-break-inside`** разрешает или запрещает разрыв страницы внутри элемента при печати.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/page-break-inside.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Страницы"

    <div class="col3" markdown="1">

    - [page-break-after](page-break-after.md)
    - [page-break-before](page-break-before.md)
    - **page-break-inside**

    </div>

    <div class="col3" markdown="1">

    - [@page](page.md)
    - [:blank](blank.md)
    - [:first](first.md)
    - [:left](left-pseudo-class.md)
    - [:right](right-pseudo-class.md)

    </div>

## Синтаксис

```css
/* Keyword values */
page-break-inside: auto;
page-break-inside: avoid;

/* Global values */
page-break-inside: inherit;
page-break-inside: initial;
page-break-inside: unset;
```

## Значения

`auto`

: Вставляет разрыв страницы при необходимости.

`avoid`

: Запрещает разрыв страницы внутри элемента.

Значение по-умолчанию: `auto`

Применяется к блочным элементам

## Спецификации

-   [CSS Paged Media Module Level 3](http://dev.w3.org/csswg/css3-page/#page-break-inside)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/page.html#propdef-page-break-inside)

## Поддержка браузерами

<p class="ciu_embed" data-feature="css-page-break" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=css-page-break">Can I Use css-page-break?</a> Data on support for the css-page-break feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>page-break-inside</title>
        <style>
            @media print {
                p {
                    page-break-inside: avoid;
                }
            }
        </style>
    </head>
    <body>
        <h2>Мусорные пакеты</h2>
        <p>
            История о том, как однажды мусорных пакетов
            оказалось несколько больше, чем хотелось, как и
            для чего их можно использовать, и что из этого
            получилось.
        </p>
        <p class="more">Читать дальше</p>
    </body>
</html>
```
