---
description: Тег option (от англ. option — пункт, параметр, опция) определяет отдельные пункты списка, создаваемого с помощью контейнера select
---

# &lt;option&gt;

Тег **`<option>`** _(от англ. **option** — пункт, параметр, опция)_ определяет отдельные пункты списка, создаваемого с помощью контейнера [`<select>`](select.md).

Ширина списка определяется самым широким текстом, указанным в `<option>`, а также может изменяться с помощью стилей. Если планируется отправлять данные списка на сервер, то требуется поместить элемент `<select>` внутрь формы. Это также необходимо, когда к данным списка идёт обращение через скрипты.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/option.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - **option**
    - [output](output.md)
    - [progress](progress.md)
    - [select](select.md)
    - [textarea](textarea.md)

    </div>

## Синтаксис

```html
<select>
    <option>Пункт 1</option>
    <option>Пункт 2</option>
</select>
```

Закрывающий тег не обязателен.

## Атрибуты

[`disabled`](#disabled)
: Заблокировать для доступа элемент списка.

[`label`](#label)
: Указание метки пункта списка.

[`selected`](#selected)
: Заранее устанавливает определённый пункт списка выделенным.

[`value`](#value)
: Значение пункта списка, которое будет отправлено на сервер или прочитано с помощью скриптов.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### disabled

Блокирует элемент списка для его выбора.

**Синтаксис**

```html
<option disabled>...</option>
```

**Значения**

Нет.

**Значение по умолчанию**

По умолчанию этот атрибут выключен.

### label

Атрибут предназначен для указания метки пункта списка, сокращённой по сравнению с текстом внутри `<option>`. Если атрибут `label` присутствует, то текст внутри `<option>` игнорируется и в списке выводится значение `label`.

**Синтаксис**

```html
<option label="<текст>">...</option>
```

**Значения**

Любая текстовая строка.

**Значение по умолчанию**

Нет.

### selected

Делает текущий пункт списка выделенным. Если к элементу [`<select>`](select.md) добавлен атрибут `multiple`, то можно выделять более одного пункта списка.

**Синтаксис**

```html
<option selected>...</option>
```

**Значения**

Нет.

**Значение по умолчанию**

По умолчанию этот атрибут выключен.

### value

Определяет значение пункта списка, которое будет отправлено на сервер. На сервер отправляется пара «`имя=значение`», где имя задаётся атрибутом name элемента [`<select>`](select.md), а значение — атрибутом `value` выделенных пунктов списка. Значение может как совпадать с текстом пункта, так быть и самостоятельным. Также атрибут `value` применяется для получения значений данных через скрипты.

**Синтаксис**

```html
<option value="<текст>">...</option>
```

**Значения**

Любая текстовая строка.

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/forms.html#the-option-element)
-   [HTML 5](http://www.w3.org/TR/html5/forms.html#the-option-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/interact/forms.html#h-17.6)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>OPTION</title>
    </head>
    <body>
        <form action="option2.php">
            <p>
                <select size="3" name="hero">
                    <option disabled>
                        Выберите рыцаря
                    </option>
                    <option value="t1" selected>
                        Гавейн
                    </option>
                    <option value="t2">Ланселот</option>
                    <option value="t3">Галахэд</option>
                    <option value="t4">Персиваль</option>
                </select>
            </p>
            <p><input type="submit" value="Отправить" /></p>
        </form>
    </body>
</html>
```

## Ссылки

-   Тег [`<option>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/option) <sup><small>MDN (рус.)</small></sup>
