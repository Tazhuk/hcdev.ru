---
description: Тег time (от англ. time — время) помечает текст внутри элемента как дату, время или оба значения
---

# &lt;time&gt;

Тег **`<time>`** _(от англ. **time** — время)_ помечает текст внутри элемента как дату, время или оба значения.

Может указываться непосредственно внутри контейнера `<time>`, либо задаваться через атрибут `datetime`.

## Демо

<iframe class="interactive is-tabbed-shorter-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/time.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - **time**
    - [u](u.md)
    - [var](var.md)
    - [wbr](wbr.md)

    </div>

## Синтаксис

```html
<time>дата и время</time>
<time datetime="<дата и время>">текст</time>
```

Закрывающий тег обязателен.

## Атрибуты

[`datetime`](#datetime)
: Задаёт дату, время или оба значения для текста.

### datetime

Устанавливает дату и время.

**Синтаксис**

```html
<time datetime="<дата и время>">Дата и время</time>
```

**Значения**

Дата и время задаётся в международном формате ISO 8601. Примеры оформления приведены в табл. 1.

<table class="table">
<caption>Табл. 1. Форматы даты и времени</caption>
<tr><th>Значение</th><th>Формат</th><th>Пример</th></tr>
<tr><td>Год</td><td>ГГГГ</td><td>2012</td></tr>
<tr><td>Месяц и год</td><td>ГГГГ-ММ</td><td>2012-12</td></tr>
<tr><td>Полная дата</td><td>ГГГГ-ММ-ДД</td><td>2012-12-23</td></tr>
<tr><td>Дата и время с минутами</td><td>ГГГГ-ММ-ДДTчч:мм</td><td>2004-07-24T18:18</td></tr>
<tr><td>Дата и время с секундами</td><td>ГГГГ-ММ-ДДTчч:мм:сс</td><td>2004-07-24T18:18:18</td></tr>
<tr><td>Дата и время с часовым поясом</td><td>ГГГГ-ММ-ДДTчч:мм:сс±чч:мм</td><td>2004-07-24T18:18:18+04:00</td></tr>
</table>

Для каждой единицы существует своя заданная форма и ограничения.

-   `Год` — задаётся четырьмя цифрами (1860).
-   `Месяц` — две цифры (01 — январь, 02 — февраль, 12 — декабрь).
-   `День` — две цифры от 01 до 31.
-   `Час` — две цифры от 00 до 23.
-   `Минуты` — две цифры от 00 до 59.
-   `Секунды` — две цифры от 00 до 59.
-   `Часовой пояс` — часы и минуты с указанием знака плюс или минус.

Дата и время разделяются между собой заглавной латинской буквой `T`. Часовой пояс при необходимости пишется после времени со знаком плюс или минус. К примеру, для Москвы часовой пояс будет +03:00.

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-time-element)
-   [HTML 5.1](https://www.w3.org/TR/2016/REC-html51-20161101/grouping-content.html#the-time-element)
-   [HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-time-element)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>time</title>
        <style>
            time {
                background: #f0f0f0;
            }
        </style>
    </head>
    <body>
        <article>
            <p>
                <time>1957-10-04</time> запущен первый
                искусственный спутник Земли.
            </p>
            <p>
                <time>1960-08-19</time> первый полёт собак в
                космос.
            </p>
            <p>
                <time>1961-04-12</time> первый полёт
                человека в космос.
            </p>
            <p>
                <time>1963-06-16</time> первый полёт
                женщины-космонавта.
            </p>
            <p>
                <time>1969-07-21</time> высадка человека на
                Луну.
            </p>
        </article>
    </body>
</html>
```

## Ссылки

-   Тег [`<time>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/time) <sup><small>MDN (рус.)</small></sup>
