---
description: Тег blockquote (от англ. block quotation - блок цитата) указывает на то, что заключенный в нем текст является развернутой цитатой
---

# &lt;blockquote&gt;

Тег **`<blockquote>`** _(от англ. **block** **quot**ation - блок цитата)_ указывает на то, что заключенный в нем текст является развернутой цитатой. URI на источник цитаты можно указать в атрибуте `cite`, тогда как текстовое представление источника может быть задано элементом [`<cite>`](cite.md).

Текст, обозначенный этим тегом, традиционно отображается как выровненный блок с отступами слева и справа (примерно по 40 пикселей), а также с отбивкой сверху и снизу.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/blockquote.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Текстовые блоки"

    <div class="col4" markdown="1">

    - **blockquote**
    - [dd](dd.md)
    - [div](div.md)
    - [dl](dl.md)
    - [dt](dt.md)
    - [hr](hr.md)
    - [li](li.md)
    - [ol](ol.md)
    - [p](p.md)
    - [pre](pre.md)
    - [ul](ul.md)

    </div>

## Синтаксис

```html
<blockquote>Цитата</blockquote>
```

Закрывающий тег обязателен.

## Атрибуты

[`cite`](#cite)

: Адрес, который указывает на источник цитаты.

Для этого элемента также доступны [универсальные атрибуты](uni-attr.md).

### cite

Задаёт адрес страницы, который указывает на источник цитаты внутри `<blockquote>`. Значение атрибута на странице не отображается и предназначено для поисковых систем.

**Синтаксис**

```html
<blockquote cite="источник цитаты">Цитата</blockquote>
```

**Значения**

Адрес.

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-blockquote-element)
-   [HTML5](http://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/text.html#h-9.2.2)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>cite</title>
    </head>
    <body>
        <p>Цитата из «Двенадцати стульев»:</p>
        <blockquote
            cite="https://ru.wikiquote.org/wiki/Двенадцать_стульев"
        >
            Неделю тому назад состоялся вечер «Общества
            спасания на водах», о чём свидетельствовал также
            лозунг на стене: Дело помощи утопающим — дело
            рук самих утопающих.
        </blockquote>
    </body>
</html>
```

## Ссылки

-   Тег [`<blockquote>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/blockquote) <sup><small>MDN (рус.)</small></sup>
