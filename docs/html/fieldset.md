---
description: Тег fieldset (от англ. field set - набор полей) предназначен для группирования элементов формы
---

# &lt;fieldset&gt;

Тег **`<fieldset>`** _(от англ. **field** **set** - набор полей)_ предназначен для группирования элементов формы.

Такая группировка облегчает работу с формами, содержащими большое число данных, например, один блок может быть предназначен для ввода текстовой информации, а другой — для флажков.

Браузеры для повышения наглядности отображают результат использования элемента `<fieldset>` в виде рамки. Её вид зависит от операционной системы, а также используемого браузера.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/fieldset.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Формы"

    <div class="col4" markdown="1">

    - [button](button.md)
    - [datalist](datalist.md)
    - **fieldset**
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

## Синтаксис

```html
<form>
    <fieldset>...</fieldset>
</form>
```

Закрывающий тег обязателен.

## Атрибуты

`disabled`

: Блокирует поля формы в группе.

`form`

: Связывает группу с формой.

`name`

: Задает имя набора полей.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### disabled

Блокирует доступ к элементам формы, расположенным внутри тега `<fieldset>`. Поля формы при этом отображаются так, словно к каждому из них добавлен атрибут `disabled`.

**Синтаксис**

```html
<fieldset disabled>...</fieldset>
```

**Значения**

Нет.

**Значение по умолчанию**

По умолчанию этот атрибут выключен.

### form

Связывает группу `<fieldset>` с формой по её идентификатору. Такая связь необходима в случае, когда элемент не располагается внутри [`<form>`](form.md), например, при создании её программно. Если установлено связывание `<form>` и `<fieldset>` между собой, то можно отправлять данные на сервер и работать с формой, как если бы элементы находились внутри формы.

**Синтаксис**

```html
<fieldset form="<идентификатор>">...</fieldset>
```

**Значения**

Идентификатор формы (значение атрибута `id` элемента `<form>`).

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-fieldset-element)
-   [HTML 5](http://www.w3.org/TR/html5/forms.html#the-fieldset-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/interact/forms.html#h-17.10)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>FIELDSET</title>
    </head>
    <body>
        <form action="handler.php">
            <fieldset>
                <legend>Работа со временем</legend>
                <input type="checkbox" /> создание
                пунктуальности (никогда не будете никуда
                опаздывать);<br />
                <input type="checkbox" /> излечение от
                пунктуальности (никогда никуда не будете
                торопиться);<br />
                <input type="checkbox" /> изменение
                восприятия времени и часов.
                <p><input type="submit" /></p>
            </fieldset>
        </form>
    </body>
</html>
```

## Ссылки

-   Тег [`<fieldset>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/fieldset) <sup><small>MDN (рус.)</small></sup>
