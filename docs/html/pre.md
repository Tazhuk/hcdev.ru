---
description: Тег pre (от англ. preformatted — предварительно отформатированный) определяет блок предварительно форматированного текста
---

# &lt;pre&gt;

Тег **`<pre>`** _(от англ. **pre**formatted — предварительно отформатированный)_ определяет блок предварительно форматированного текста.

Такой текст отображается обычно моноширинным шрифтом и со всеми пробелами между словами. По умолчанию, любое количество пробелов идущих в коде подряд, на веб-странице показывается как один. Элемент `<pre>` позволяет обойти эту особенность и отображать текст как требуется разработчику.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/pre.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Текстовые блоки"

    <div class="col4" markdown="1">

    - [blockquote](blockquote.md)
    - [dd](dd.md)
    - [div](div.md)
    - [dl](dl.md)
    - [dt](dt.md)
    - [hr](hr.md)
    - [li](li.md)
    - [ol](ol.md)
    - [p](p.md)
    - **pre**
    - [ul](ul.md)

    </div>

## Синтаксис

```html
<pre>Текст</pre>
```

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-pre-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-pre-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/text.html#h-9.3.4)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>PRE</title>
    </head>
    <body>
        <pre>
-                -----  
-----           |-----
||----|          ----||  
||-----         -----||  
||-----|       |-----||
|| -----       ------||
||- ----|     |------||
||---||--     -------||
||--|| --|   |-------||
|| -|| |--   --- - --||
|| -||  --|-|--| - ---|
|---||  |-----| |-----|
|---||   |----  |-----|
|----|    ---   |-----|
|-----          ------|
</pre
        >
    </body>
</html>
```

## Ссылки

-   Тег [`<pre>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/pre) <sup><small>MDN (рус.)</small></sup>
