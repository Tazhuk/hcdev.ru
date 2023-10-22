---
description: Тег output (от англ. output — вывод) определяет область, в которую выводится информация, преимущественно с помощью скриптов
---

# &lt;output&gt;

Тег **`<output>`** _(от англ. **output** — вывод)_ определяет область, в которую выводится информация, преимущественно с помощью скриптов.

Полифилы для включения поддержки:

-   [`<output>` polyfill](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills#output-progress-menu-command)

??? info "Формы"

    <div class="col4" markdown="1">

    - [button](button.md)
    - [datalist](datalist.md)
    - [fieldset](fieldset.md)
    - [form](form.md)
    - [input](input.md)
    - [label](label.md)
    - [legend](legend.md)
    - [meter](meter.md)
    - [optgroup](optgroup.md)
    - [option](option.md)
    - **output**
    - [progress](progress.md)
    - [select](select.md)
    - [textarea](textarea.md)

    </div>

## Синтаксис

```html
<output> </output>
```

Закрывающий тег обязателен.

## Атрибуты

`for`

: Определяет идентификатор одного и более элементов для связывания с элементом `<output>`.

`form`

: Задаёт имя формы, которой принадлежит область для вывода.

`name`

: Задаёт уникальное имя элемента.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-output-element)
-   [HTML 5](http://www.w3.org/TR/html5/forms.html#the-output-element)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>output</title>
    </head>
    <body>
        <form
            oninput="result.value=(cm.value/2.54).toFixed(2)"
        >
            <p>
                Введите длину в сантиметрах:
                <input type="number" name="cm" autofocus />
            </p>
            <p>
                Длина в дюймах:
                <output name="result">0</output>
            </p>
        </form>
    </body>
</html>
```

## Ссылки

-   Тег [`<output>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/output) <sup><small>MDN (рус.)</small></sup>
