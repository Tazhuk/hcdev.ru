---
description: Свойство resize указывает, можно ли пользователю изменять размеры текстового поля
---

# resize

Свойство **`resize`** указывает, можно ли пользователю изменять размеры текстового поля.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/resize.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Интерфейс"

    <div class="col3" markdown="1">

    - [appearance](appearance.md)
    - [box-sizing](box-sizing.md)
    - [caret-color](caret-color.md)
    - [cursor](cursor.md)
    - [outline](outline.md)
    - [outline-width](outline-width.md)
    - [outline-style](outline-style.md)
    - [outline-color](outline-color.md)
    - [outline-offset](outline-offset.md)
    - **resize**
    - [text-overflow](text-overflow.md)
    - [user-select](user-select.md)

    </div>

## Синтаксис

```css
/* Keyword values */
resize: none;
resize: both;
resize: horizontal;
resize: vertical;
resize: block;
resize: inline;

/* Global values */
resize: inherit;
resize: initial;
resize: revert;
resize: revert-layer;
resize: unset;s
```

## Значения

`none`

: Размеры элемента не изменяются.

`both`

: Можно изменять размеры элемента по горизонтали и вертикали.

`horizontal`

: Можно изменять размеры элемента только по горизонтали.

`vertical`

: Можно изменять размеры элемента только по вертикали.

### Примечание

Хотя по умолчанию значение установлено как `none`, многие браузеры самостоятельно меняют его на `both`. Если вы не хотите, чтобы размер поля изменялся, задавайте явное значение `none`, а не оставляйте его по умолчанию.

Значение по-умолчанию: `none`

Применяется к [`<textarea>`](../html/textarea.md) или к любому элементу, у которого свойство [`overflow`](overflow.md) отличается от `visible`

## Спецификации

-   [CSS Basic User Interface Module Level 4](https://w3c.github.io/csswg-drafts/css-ui/#resize)
-   [CSS Basic User Interface Module Level 3](http://dev.w3.org/csswg/css3-ui/#resize)

## Поддержка браузерами

<p class="ciu_embed" data-feature="css-resize" data-periods="future_1,current,past_1,past_2"></p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>resize</title>
        <style>
            textarea {
                resize: both;
            }
        </style>
    </head>
    <body>
        <p>
            Потяните за правый уголок, чтобы изменить размер
            текстового поля.
        </p>
        <p><textarea cols="30" rows="7"></textarea></p>
    </body>
</html>
```
