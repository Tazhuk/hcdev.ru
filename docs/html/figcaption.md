---
description: Тег figcaption (от англ. figure caption - подпись к рисунку) содержит описание для элемента figure
---

# &lt;figcaption&gt;

Тег **`<figcaption>`** _(от англ. **fig**ure **caption** - подпись к рисунку)_ содержит описание для элемента [`<figure>`](figure.md).

`<figcaption>` должен быть первым или последним элементом в группе.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/figcaption.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения и мультимедиа"

    <div class="col4" markdown="1">

    - [area](area.md)
    - [audio](audio.md)
    - [img](img.md)
    - **figcaption**
    - [figure](figure.md)
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
<figure>
    <figcaption>Описание</figcaption>
</figure>
```

Закрывающий тег обязателен.

## Атрибуты

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-figcaption-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element)

## Описание и примеры

### Пример 1

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>FIGCAPTION</title>
        <style>
            figure {
                background: #d9dabb; /* Цвет фона */
                display: block; /* Блочный элемент */
                width: 150px; /* Ширина */
                height: 190px; /* Высота */
                float: left; /* Блоки выстраиваются по горизонтали */
                margin: 0 10px 10px 0; /* Отступы */
                text-align: center; /* Выравнивание по центру */
            }
            figure img {
                border: 2px solid #8b8e4b; /* Параметры рамки */
            }
            figure p {
                margin-bottom: 0; /* Отступ снизу */
            }
        </style>
    </head>
    <body>
        <article>
            <figure>
                <p><img src="image/thumb3.jpg" alt="" /></p>
                <figcaption>Купеческий клуб</figcaption>
            </figure>
            <figure>
                <p><img src="image/thumb4.jpg" alt="" /></p>
                <figcaption>
                    Памятник Св. Владимиру
                </figcaption>
            </figure>
        </article>
    </body>
</html>
```

### Пример 2

```html
<!-- Just a figure -->
<figure>
    <img
        src="https://developer.cdn.mozilla.net/media/img/mdn-logo-sm.png"
        alt="An awesome picture"
    />
</figure>
<p></p>
<!-- Figure with figcaption -->
<figure>
    <img
        src="https://developer.cdn.mozilla.net/media/img/mdn-logo-sm.png"
        alt="An awesome picture"
    />
    <figcaption>Fig1. MDN Logo</figcaption>
</figure>
<p></p>
```

## Ссылки

-   Тег [`<figcaption>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/figcaption) <sup><small>MDN (рус.)</small></sup>
