---
description: Тег li (от англ. list item - пункт списка) определяет отдельный пункт списка
---

# &lt;li&gt;

Тег **`<li>`** _(от англ. **l**ist **i**tem — пункт списка)_ определяет отдельный пункт списка. Внешний элемент [`<ul>`](ul.md) или [`<ol>`](ol.md) устанавливает тип списка — маркированный или нумерованный.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/li.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Текстовые блоки"

    <div class="col4" markdown="1">

    - [blockquote](blockquote.md)
    - [dd](dd.md)
    - [div](div.md)
    - [dl](dl.md)
    - [dt](dt.md)
    - [hr](hr.md)
    - **li**
    - [ol](ol.md)
    - [p](p.md)
    - [pre](pre.md)
    - [ul](ul.md)

    </div>

## Синтаксис

```html
<ul>
    <li>элемент маркированного списка</li>
</ul>

<ol>
    <li>элемент нумерованного списка</li>
</ol>
```

Закрывающий тег не обязателен.

## Атрибуты

[`value`](#value)
: Число, с которого будет начинаться нумерованный список.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### value

Атрибут `value` устанавливает номер, с которого будет начинаться список. `value` применяется только для нумерованных списков, когда элемент `<li>` находится внутри контейнера [`<ol>`](ol.md). При этом не имеет значения, какой тип списка установлен с помощью `type`, атрибут `value` одинаково работает и с римскими и с арабскими числами.

**Синтаксис**

```html
<li value="<число>">...</li>
```

**Значения**

Любое целое положительное число.

**Значение по умолчанию**

`1`

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-li-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-li-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/lists.html#h-10.2)

## Описание и примеры

```html
<ol type="I">
    <li value="3">Третий элемент</li>
    <li>Четвёртый элемент</li>
    <li>Пятый элемент</li>
</ol>
```

## Ссылки

-   Тег [`<li>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/li) <sup><small>MDN (рус.)</small></sup>
