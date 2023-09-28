---
description: Тег head (от англ. head - голова) предназначен для хранения других элементов, цель которых — помочь браузеру в работе с данными
---

# &lt;head&gt;

Тег **`<head>`** _(от англ. **head** — голова)_ предназначен для хранения других элементов, цель которых — помочь браузеру в работе с данными.

Также внутри контейнера `<head>` находятся метатеги, которые используются для хранения информации предназначенной для браузеров и поисковых систем. Например, механизмы поисковых систем обращаются к метатегам для получения описания сайта, ключевых слов и других данных.

Содержимое `<head>` не отображается напрямую на веб-странице, за исключением элемента [`<title>`](title.md), он задаёт заголовок окна веб-страницы.

Внутри контейнера `<head>` допускается размещать следующие элементы: [`<base>`](base.md), [`<link>`](link.md), [`<meta>`](meta.md), [`<script>`](script.md), [`<style>`](style.md), [`<title>`](title.md).

??? info "Основные элементы"

    <div class="col4" markdown="1">

    - [html](html.md)
    - **head**
    - [body](body.md)

    </div>

## Синтаксис

```html
<head>
    ...
</head>
```

Закрывающий тег не обязателен.

## Атрибуты

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-head-element)
-   [HTML5](http://www.w3.org/TR/html5/document-metadata.html#the-head-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/global.html#h-7.4.1)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Этот раздел предназначен для заголовка страницы
	     и технической информации. -->
    </head>

    <body>
        <!-- А здесь надо размещать всё,
	     что хочется увидеть на странице. -->
    </body>
</html>
```

## Ссылки

-   Тег [`<head>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/head) <sup><small>MDN (рус.)</small></sup>
