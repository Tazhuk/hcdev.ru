---
description: Свойство CSS overflow-inline устанавливает, что будет отображаться, когда содержимое выходит за пределы встроенных начального и конечного краев блока. Это может быть ничего, полоса прокрутки или содержимое переполнения.
---

# overflow-inline

Свойство **`overflow-inline`** устанавливает, что будет отображаться, когда содержимое выходит за пределы встроенных начального и конечного краев блока. Это может быть ничего, полоса прокрутки или содержимое переполнения.

??? info "Логические блоки"

    <div class="col3" markdown="1">

    - [margin-block](margin-block.md)
    - [margin-block-end](margin-block-end.md)
    - [margin-block-start](margin-block-start.md)
    - [margin-inline](margin-inline.md)
    - [margin-inline-end](margin-inline-end.md)
    - [margin-inline-start](margin-inline-start.md)

    </div>

    <div class="col3" markdown="1">

    - [overflow-block](overflow-block.md)
    - **overflow-inline**

    </div>

    <div class="col3" markdown="1">

    - [padding-block](padding-block.md)
    - [padding-block-end](padding-block-end.md)
    - [padding-block-start](padding-block-start.md)
    - [padding-inline](padding-inline.md)
    - [padding-inline-end](padding-inline-end.md)
    - [padding-inline-start](padding-inline-start.md)

    </div>

## Синтаксис

```css
/* Keyword values */
overflow-inline: visible;
overflow-inline: hidden;
overflow-inline: scroll;
overflow-inline: auto;

/* Global values */
overflow-inline: inherit;
overflow-inline: initial;
overflow-inline: revert;
overflow-inline: revert-layer;
overflow-inline: unset;
```

## Значения

`visible`

: Содержимое не обрезается и может отображаться за пределами начального и конечного краев блока поля заполнения.

`hidden`

: Содержимое обрезается, если необходимо, чтобы соответствовать размеру блока в поле заполнения. Полосы прокрутки не предусмотрены.

`scroll`

: Содержимое обрезается, если это необходимо, чтобы соответствовать размеру блока в поле заполнения. Браузеры отображают полосы прокрутки независимо от того, обрезано ли какое-либо содержимое. (Это предотвратит появление или исчезновение полос прокрутки при изменении содержимого.) Принтеры могут по-прежнему печатать переполненное содержимое.

`auto`

: Зависит от пользовательского агента. Если содержимое помещается внутри поля заполнения, оно выглядит так же, как `visible`, но по-прежнему устанавливает новый контекст форматирования блока. Настольные браузеры предоставляют полосы прокрутки, если содержимое выходит за пределы.

## Поддержка браузерами

<p class="ciu_embed" data-feature="mdn-css__properties__overflow-inline" data-periods="future_1,current,past_1,past_2" data-accessible-colours="false"></p>

## Ссылки

-   Свойство [`overflow-inline`](https://developer.mozilla.org/ru/docs/Web/CSS/overflow-inline) <sup><small>MDN (рус.)</small></sup>
-   [CSS Overflow Module Level 3](https://w3c.github.io/csswg-drafts/css-overflow/#logical) <sup><small>Spec (англ.)</small></sup>
