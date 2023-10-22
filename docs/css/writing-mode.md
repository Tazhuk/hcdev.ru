---
description: Свойство CSS write-mode определяет, будут ли строки текста располагаться горизонтально или вертикально, а также направление, в котором перемещаются блоки.
---

# writing-mode

Свойство **`writing-mode`** устанавливает горизонтальное или вертикальное положение текста также как и направление блока.

Свойство определяет направление потока блока, в каком направлении складываются контейнеры уровня блока и направление в котором инлайновый контент находится в родительском блоке. Также свойство `writing-mode` определяет порядок контента блочного уровня.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/writing-mode.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Режимы письма"

    <div class="col3" markdown="1">

    - [direction](direction.md)
    - [text-combine-upright](text-combine-upright.md)
    - [text-orientation](text-orientation.md)
    - [unicode-bidi](unicode-bidi.md)
    - **writing-mode**

    </div>

| Начальное значение | horizontal-tb |
| --- | --- |
| Применяется к | все элементы, кроме групп табличных строк, групп табличных столбцов, табличных строк и табличных колонок |
| Наследуется | да |
| Обработка значения | как указано |
| Animation type | discrete |

## Синтаксис

```css
/* Keyword values */
writing-mode: horizontal-tb;
writing-mode: horizontal-bt;
writing-mode: vertical-rl;
writing-mode: vertical-lr;

/* Global values */
writing-mode: inherit;
writing-mode: initial;
writing-mode: unset;
```

## Значения

`horizontal-tb`

: Контент располагается горизонтально слева направо, вертикально сверху вниз. Следующая горизонтальная линия расположена под предыдущей линией.

`horizontal-bt`

: Контент располагается горизонтально слева направо, вертикально со внизу вверх. Следующая горизонтальная линия расположена над предыдущей линией.

`vertical-rl`

: Контент располагается вертикально сверху вниз, горизонтально справа налево. Следующая вертикальная линия расположена слева от предыдущей линии.

`vertical-lr`

: Контент располагается вертикально сверху вниз, горизонтально слева направо. Следующая вертикальная линия расположена справа от предыдущей линии.

## Спецификации

-   [CSS Writing Modes Module Level 3](https://drafts.csswg.org/css-writing-modes-3/#block-flow)
