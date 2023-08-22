---
description: Тег datalist (от англ. list of data - список данных) создаёт список вариантов, которые можно выбирать при наборе в текстовом поле
---

# &lt;datalist&gt;

Тег **`<datalist>`** _(от англ. **list** of **data** - список данных)_ создаёт список вариантов, которые можно выбирать при наборе в текстовом поле. Изначально этот список скрыт и становится доступным при получении полем фокуса или при наборе текста.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/datalist.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Формы"

    <div class="col4" markdown="1">

    - [button](button.md)
    - **datalist**
    - [fieldset](fieldset.md)
    - [form](form.md)
    - [input](input.md)
    - [label](label.md)
    - [legend](legend.md)
    - [meter](meter.md)
    - [optgroup](optgroup.md)
    - [option](option.md)
    - [output](output.md)
    - [progress](progress.md)
    - [select](select.md)
    - [textarea](textarea.md)

    </div>

## Поддержка браузерами

<p class="ciu_embed" data-feature="datalist" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=datalist">Can I Use datalist?</a> Data on support for the datalist feature across the major browsers from caniuse.com.
</p>

## Синтаксис

```html
<input list="<идентификатор>" />
<datalist id="<идентификатор>">
    <option value="Текст1"></option>
    <option value="Текст2"></option>
</datalist>
```

Закрывающий тег обязателен.

## Атрибуты

Список, создаваемый элементом `<datalist>`, связывается с текстовым полем посредством атрибута `id`. Его значение должно совпадать со значением атрибута `list` элемента [`<input>`](input.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-datalist-element)
-   [HTML5](http://www.w3.org/TR/html5/forms.html#the-datalist-element)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>datalist</title>
    </head>
    <body>
        <p>Выберите любимого персонажа:</p>
        <p>
            <input list="character" />
            <datalist id="character">
                <option value="Чебурашка"></option>
                <option value="Крокодил Гена"></option>
                <option value="Шапокляк"></option>
            </datalist>
        </p>
    </body>
</html>
```

## Ссылки

-   Тег [`<datalist>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/datalist) <sup><small>MDN (рус.)</small></sup>
