---
description: Тег p (от англ. paragraph — параграф) определяет текстовый абзац
---

# &lt;p&gt;

Тег **`<p>`** _(от англ. **p**aragraph — параграф)_ определяет текстовый абзац.

Элемент `<p>` является блочным, всегда начинается с новой строки, абзацы текста идущие друг за другом разделяются между собой отбивкой. Величиной отбивки можно управлять с помощью стилей. Если закрывающего тега нет, считается, что конец абзаца совпадает с началом следующего абзаца или другого блочного элемента.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/p.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - **p**
    - [pre](pre.md)
    - [ul](ul.md)

    </div>

## Синтаксис

```html
<p>Текст</p>
```

Закрывающий тег не обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-p-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-p-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/text.html#h-9.3.1)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>P</title>
    </head>
    <body>
        <p>
            Рекомендуется совершить прогулку на лодке по
            каналам города и Озеру Любви.
        </p>
        <p>
            Венгры страстно любят танцевать, особенно
            ценятся национальные танцы.
        </p>
        <p>
            Из первых блюд распространены супы-пюре и
            бульоны, но подают их редко.
        </p>
    </body>
</html>
```

## Ссылки

-   Тег [`<p>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/p) <sup><small>MDN (рус.)</small></sup>
