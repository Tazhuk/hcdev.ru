---
description: Тег dfn (от англ. definition - термин, определение) применяется для выделения терминов при их первом появлении в тексте
---

# &lt;dfn&gt;

Тег **`<dfn>`** _(от англ. **d**e**f**i**n**ition - термин, определение)_ применяется для выделения терминов при их первом появлении в тексте. Как правило, в документе, когда упоминается новый термин, он выделяется курсивом и даётся его определение. При использовании этого термина в дальнейшем, он считается уже известным читателю.

Браузеры, чаще всего отображают содержимое контейнера `<dfn>` с помощью курсивного начертания.

Определение термина задаётся с помощью атрибута `title` у элемента `<dfn>`, либо с помощью атрибута `title` у вложенного элемента [`<abbr>`](abbr.md), либо текстом внутри `<dfn>`.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/dfn.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Текстовые элементы"

    <div class="col4" markdown="1">

    - [a](a.md)
    - [abbr](abbr.md)
    - [b](b.md)
    - [bdi](bdi.md)
    - [bdo](bdo.md)
    - [br](br.md)
    - [cite](cite.md)
    - [code](code.md)
    - [data](data.md)
    - [del](del.md)
    - **dfn**
    - [em](em.md)
    - [i](i.md)
    - [ins](ins.md)
    - [kbd](kbd.md)
    - [mark](mark.md)
    - [q](q.md)
    - [ruby](ruby.md)
    - [rtc](rtc.md)
    - [rb](rb.md)
    - [rp](rp.md)
    - [rt](rt.md)
    - [s](s.md)
    - [samp](samp.md)
    - [small](small.md)
    - [span](span.md)
    - [strong](strong.md)
    - [sub](sub.md)
    - [sup](sup.md)
    - [time](time.md)
    - [u](u.md)
    - [var](var.md)
    - [wbr](wbr.md)

    </div>

## Синтаксис

```html
<dfn>Текст</dfn>
```

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-dfn-element)
-   [HTML5](http://www.w3.org/TR/html5/text-level-semantics.html#the-dfn-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/text.html#h-9.2.1)

## Описание и примеры

### Пример 1

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>DFN</title>
    </head>
    <body>
        <p>
            <dfn>Капителью</dfn> в типографике называется
            текст, набранный прописными буквами уменьшенного
            размера.
        </p>
    </body>
</html>
```

### Пример 2

```html
<!-- Define "The Internet" -->
<p>
    <dfn id="def-internet">The Internet</dfn> is a global
    system of interconnected networks that use the Internet
    Protocol Suite (TCP/IP) to serve billions of users
    worldwide.
</p>
```

Далее в этом же документе:

```html
<dl>
    <!-- Define "World-Wide Web" and reference
		definition for "the Internet" -->
    <dt>
        <dfn>
            <abbr title="World-Wide Web">WWW</abbr>
        </dfn>
    </dt>
    <dd>
        The World-Wide Web (WWW) is a system of interlinked
        hypertext documents accessed on
        <a href="#def-internet">the Internet</a>.
    </dd>
</dl>
```

## Ссылки

-   Тег [`<dfn>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/dfn) <sup><small>MDN (рус.)</small></sup>
