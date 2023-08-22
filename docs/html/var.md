---
description: Тег var (от англ. variable — переменная) используется для выделения переменных из компьютерных программ
---

# &lt;var&gt;

Тег **`<var>`** _(от англ. **var**iable — переменная)_ используется для выделения переменных из компьютерных программ.

Браузеры обычно помечают текст в контейнере `<var>` курсивным начертанием.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/var.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - [dfn](dfn.md)
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
    - **var**
    - [wbr](wbr.md)

    </div>

## Синтаксис

```html
<var>Текст</var>
```

Закрывающий тег обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-var-element)
-   [HTML 5](http://www.w3.org/TR/html5/textlevel-semantics.html#the-var-element)

## Примеры

### Пример 1

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>VAR</title>
    </head>
    <body>
        <p>
            В данном примере делается запрос к базе данных
            для получения поля
            <var>content_title</var> из таблицы
            <var>content</var>, причем должно
            удовлетворяться условие
            <code>section_id = 1</code>.
        </p>
    </body>
</html>
```

### Пример 2

Вот простой пример использования `<var>` для обозначения имен переменных в математическом уравнении.

```html
<p>A simple equation: <var>x</var> = <var>y</var> + 2</p>
```

### Пример 3

Используя CSS, вы можете переопределить стиль по умолчанию для элемента `<var>`. В этом примере имена переменных отображаются с использованием полужирного Courier, если он доступен, в противном случае он возвращается к моноширинному шрифту по умолчанию.

=== "HTML"

    ```html
    <p>
      The variables <var>minSpeed</var> and
      <var>maxSpeed</var> control the minimum and maximum speed
      of the apparatus in revolutions per minute (RPM).
    </p>
    ```

=== "CSS"

    ```css
    var {
      font: bold 15px 'Courier', 'Courier New', monospace;
    }
    ```

## Ссылки

-   Тег [`<var>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/var) <sup><small>MDN (рус.)</small></sup>
