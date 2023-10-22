---
description: Свойство paint-order позволяет вам контролировать порядок, в котором отрисовываются заливка и обводка (и нарисованные маркеры) текстового содержимого и фигур
---

# paint-order

Свойство **`paint-order`** позволяет вам контролировать порядок, в котором отрисовываются заливка и обводка (и нарисованные маркеры) текстового содержимого и фигур.

??? info "Текст"

    <div class="col3" markdown="1">

    - [hanging-punctuation](hanging-punctuation.md)
    - [hyphens](hyphens.md)
    - [letter-spacing](letter-spacing.md)
    - [line-break](line-break.md)
    - [overflow-wrap](overflow-wrap.md)
    - **paint-order**
    - [tab-size](tab-size.md)
    - [text-align](text-align.md)
    - [text-align-last](text-align-last.md)
    - [text-indent](text-indent.md)
    - [text-justify](text-justify.md)
    - [text-size-adjust](text-size-adjust.md)
    - [text-transform](text-transform.md)
    - [white-space](white-space.md)
    - [word-break](word-break.md)
    - [word-spacing](word-spacing.md)

    </div>

    <div class="col3" markdown="1">

    - [letter-spacing](letter-spacing.md)
    - [text-decoration](text-decoration.md)
    - [text-decoration-color](text-decoration-color.md)
    - [text-decoration-line](text-decoration-line.md)
    - [text-decoration-style](text-decoration-style.md)
    - [text-decoration-thickness](text-decoration-thickness.md)
    - [text-decoration-skip](text-decoration-skip.md)
    - [text-decoration-skip-ink](text-decoration-skip-ink.md)
    - [text-emphasis](text-emphasis.md)
    - [text-emphasis-color](text-emphasis-color.md)
    - [text-emphasis-position](text-emphasis-position.md)
    - [text-emphasis-style](text-emphasis-style.md)
    - [text-indent](text-indent.md)
    - [text-rendering](text-rendering.md)
    - [text-shadow](text-shadow.md)
    - [text-underline-position](text-underline-position.md)
    - [text-transform](text-transform.md)
    - [white-space](white-space.md)
    - [word-spacing](word-spacing.md)

    </div>

## Синтаксис

```css
/* Normal */
paint-order: normal;

/* Single values */
paint-order: stroke; /* draw the stroke first, then fill and markers */
paint-order: markers; /* draw the markers first, then fill and stroke */

/* Multiple values */
paint-order: stroke fill; /* draw the stroke first, then the fill, then the markers */
paint-order: markers stroke fill; /* draw markers, then stroke, then fill */

/* Global values */
paint-order: inherit;
paint-order: initial;
paint-order: revert;
paint-order: unset;
```

Если значение не указано, значением по умолчанию является следующий порядок `fill`, `stroke`, `markers`.

Когда указано одно значение, то сначала отрисовывается оно, затем два других в дефолтном поряд друг относительно друга. Когда указано два значения, они будут отрисованы в указанном порядке, а затем будет отрисовано неопределенное значение.

## Значения

`normal`

: Окрасит различные части в обычном порядке.

`stroke`, `fill`, `markers`

: Указываются некоторые или все эти значения в том порядке, в котором вы хотите увидеть отрисовку.

## Спецификация

-   [Scalable Vector Graphics (SVG) 2](https://svgwg.org/svg2-draft/painting.html#PaintOrder)

## Поддержка браузерами

<p class="ciu_embed" data-feature="mdn-css__properties__paint-order" data-periods="future_1,current,past_1,past_2" data-accessible-colours="false"></p>

## Пример

=== "SVG"

    ```xml
    <svg xmlns="http://www.w3.org/2000/svg" width="400" height="200">
      <text x="10" y="75">stroke in front</text>
      <text x="10" y="150" class="stroke-behind">stroke behind</text>
    </svg>
    ```

=== "CSS"

    ```css
    text {
      font-family: sans-serif;
      font-size: 50px;
      font-weight: bold;
      fill: black;
      stroke: red;
      stroke-width: 4px;
    }

    .stroke-behind {
      paint-order: stroke fill;
    }
    ```
