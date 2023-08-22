---
description: Тег figure (от англ. figure - рисунок) используется для группирования любых элементов, например, изображений и подписей к ним
---

# &lt;figure&gt;

Тег **`<figure>`** _(от англ. **figure** - рисунок)_ используется для группирования любых элементов, например, изображений и подписей к ним.

`<figure>` не должен быть связан непосредственно с основным содержимым документа и при его перемещении в другое место смысл текста не должен меняться. Обычно применяется для иллюстраций, фрагментов кода, схем, графиков, диаграмм и др.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/figure.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения и мультимедиа"

    <div class="col4" markdown="1">

    - [area](area.md)
    - [audio](audio.md)
    - [img](img.md)
    - [figcaption](figcaption.md)
    - **figure**
    - [map](map.md)
    - [track](track.md)
    - [video](video.md)
    - [embed](embed.md)
    - [iframe](iframe.md)
    - [object](object.md)
    - [param](param.md)
    - [picture](picture.md)
    - [source](source.md)

    </div>

## Синтаксис

```html
<figure>...</figure>
```

Закрывающий тег обязателен.

## Атрибуты

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-figure-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>FIGURE</title>
        <style>
            figure {
                background: #5f6a72; /* Цвет фона */
                padding: 10px; /* Поля вокруг */
                width: 150px; /* Ширина */
                float: left; /* Блоки выстраиваются по горизонтали */
                margin: 0 10px 10px 0; /* Отступы */
                text-align: center; /* Выравнивание по центру */
            }
            figcaption {
                color: #fff; /* Цвет текста */
            }
        </style>
    </head>
    <body>
        <article>
            <figure>
                <p><img src="image/thumb1.jpg" alt="" /></p>
                <figcaption>Софийский собор</figcaption>
            </figure>
            <figure>
                <p><img src="image/thumb2.jpg" alt="" /></p>
                <figcaption>Польский костел</figcaption>
            </figure>
        </article>
    </body>
</html>
```

## Ссылки

-   Тег [`<figure>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/figure) <sup><small>MDN (рус.)</small></sup>
