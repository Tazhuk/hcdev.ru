---
description: Тег legend (от англ. legend - легенда, надпись) применяется для создания заголовка группы элементов формы, которая определяется с помощью fieldset
---

# &lt;legend&gt;

Тег **`<legend>`** _(от англ. **legend** — легенда, надпись)_ применяется для создания заголовка группы элементов формы, которая определяется с помощью [`<fieldset>`](fieldset.md).

Группа элементов обозначается в браузере с помощью рамки, а текст, который располагается внутри контейнера `<legend>`, встраивается в эту рамку.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/legend.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Формы"

    <div class="col4" markdown="1">

    - [button](button.md)
    - [datalist](datalist.md)
    - [fieldset](fieldset.md)
    - [form](form.md)
    - [input](input.md)
    - [label](label.md)
    - **legend**
    - [meter](meter.md)
    - [optgroup](optgroup.md)
    - [option](option.md)
    - [output](output.md)
    - [progress](progress.md)
    - [select](select.md)
    - [textarea](textarea.md)

    </div>

## Синтаксис

```html
<fieldset>
    <legend>Текст</legend>
</fieldset>
```

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-label-element)
-   [HTML 5](http://www.w3.org/TR/html5/forms.html#the-label-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/interact/forms.html#h-17.9.1)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>LEGEND</title>
    </head>
    <body>
        <fieldset>
            <legend>Работа со временем</legend>
            <p>
                <input type="checkbox" /> создание
                пунктуальности (никогда не будете никуда
                опаздывать);<br />
                <input type="checkbox" /> излечение от
                пунктуальности (никогда никуда не будете
                торопиться);<br />
                <input type="checkbox" /> изменение
                восприятия времени и часов.
            </p>
        </fieldset>
    </body>
</html>
```

## Ссылки

-   Тег [`<legend>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/legend) <sup><small>MDN (рус.)</small></sup>
