---
description: Свойства unicode-bidi и direction задают, как должен располагаться текст используемого языка
---

# unicode-bidi

Свойства **`unicode-bidi`** и [`direction`](direction.md) задают, как должен располагаться текст используемого языка.

В европейских языках чтение текста происходит слева направо, в то время как есть языки, где текст читается справа налево. При смешении в одном документе разных по написанию символов (русского с ивритом, к примеру) в системе юникод, их направление определяется браузером из характеристик и содержимого текста.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/unicode-bidi.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Режимы письма"

    <div class="col3" markdown="1">

    - [direction](direction.md)
    - [text-combine-upright](text-combine-upright.md)
    - [text-orientation](text-orientation.md)
    - **unicode-bidi**
    - [writing-mode](writing-mode.md)

    </div>

## Синтаксис

```css
/* Keyword values */
unicode-bidi: normal;
unicode-bidi: embed;
unicode-bidi: isolate;
unicode-bidi: bidi-override;
unicode-bidi: isolate-override;
unicode-bidi: plaintext;
/* Global values */
unicode-bidi: inherit;
unicode-bidi: initial;
unicode-bidi: unset;
```

## Значения

`normal`

: Браузер самостоятельно определяет, как ему следует отображать текст на основе символов юникода.

`embed`

: Переопределяет параметры текста, располагая его, как указано в свойстве `direction`.

`bidi-override`

: Аналогичен `embed`, но при этом также меняется порядок символов в тексте, подчиняясь значению `direction`.

Значение по-умолчанию:

```css
unicode-bidi: normal;
```

Применяется ко всем элементам

## Спецификации

-   [CSS Writing Modes Module Level 3](http://dev.w3.org/csswg/css3-writing-modes/#unicode-bidi)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#propdef-unicode-bidi)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>unicode-bidi</title>
        <style>
            .rtl p {
                unicode-bidi: bidi-override; /* Меняются характеристики текста */
                direction: rtl; /* Текст пишется справа налево */
            }
        </style>
    </head>
    <body>
        <div class="rtl">
            <p>А роза упала на лапу Азора.</p>
            <p>У лип Леша нашел пилу.</p>
            <p>И городу дорог огород у дороги.</p>
            <p>Уж я веники не вяжу.</p>
            <p>Аргентина манит негра.</p>
            <p>
                Он дивен, палиндром — и ни морд, ни лап не
                видно.
            </p>
            <p>
                Но невидим архангел, мороз узором лег на
                храм и дивен он.
            </p>
            <p>Леша на полке клопа нашел.</p>
            <p>Я не стар брат Сеня.</p>
        </div>
    </body>
</html>
```
