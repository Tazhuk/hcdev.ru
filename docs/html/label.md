---
description: Тег label (от англ. label - метка, ярлык) устанавливает связь между определённой меткой, в качестве которой обычно выступает текст, и элементом формы input, select, textarea
---

# &lt;label&gt;

Тег **`<label>`** _(от англ. **label** — метка, ярлык)_ устанавливает связь между определённой меткой, в качестве которой обычно выступает текст, и элементом формы ([`<input>`](input.md), [`<select>`](select.md), [`<textarea>`](textarea.md)).

Такая связь необходима, чтобы изменять значения элементов формы при щелчке курсором мыши на текст. Кроме того, с помощью `<label>` можно устанавливать горячие клавиши на клавиатуре и переходить на активный элемент подобно ссылкам.

Существует два способа связывания объекта и метки. Первый заключается в использовании идентификатора `id` внутри элемента формы и указании его имени в качестве атрибута `for` элемента `<label>`. При втором способе элемент формы помещается внутрь контейнера `<label>`.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/label.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Формы"

    <div class="col4" markdown="1">

    - [button](button.md)
    - [datalist](datalist.md)
    - [fieldset](fieldset.md)
    - [form](form.md)
    - [input](input.md)
    - **label**
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
<input id="<идентификатор>" /><label for="<идентификатор>"
    >Текст</label
>
<label><input /> Текст</label>
```

Закрывающий тег обязателен.

## Атрибуты

[`for`](#for)

: Идентификатор элемента, с которым следует установить связь.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### for

Задаёт уникальный идентификатор, определяемый с помощью атрибута `id` элемента [`<input>`](input.md), с которым следует установить связь. Атрибут `for` необходимо задавать в том случае, когда элемент формы и текст разделены. Если `<input>` размещается внутри контейнера `<label>`, то применять атрибут `for` не требуется.

**Синтаксис**

```html
<label for="<идентификатор>">...</label>
```

**Значения**

Имя идентификатора. Такое имя чувствительно к регистру, поэтому его следует писать так же, как оно описано внутри элемента `<input>`.

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-label-element)
-   [HTML 5](http://www.w3.org/TR/html5/forms.html#the-label-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/interact/forms.html#h-17.9.1)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>LABEL</title>
    </head>
    <body>
        <form action="handler.php">
            <p><b>Выберите напиток</b></p>
            <p>
                <input type="checkbox" id="check1" /><label
                    for="check1"
                    >Коньяк</label
                ><br />
                <input type="checkbox" id="check2" /><label
                    for="check2"
                    >Арманьяк</label
                ><br />
                <input type="checkbox" id="check3" /><label
                    for="check3"
                    >Кальвадос</label
                ><br />
            </p>
        </form>
    </body>
</html>
```

## Ссылки

-   Тег [`<label>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/label) <sup><small>MDN (рус.)</small></sup>
