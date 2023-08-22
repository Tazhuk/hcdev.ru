---
description: Тег dd (от англ. definition description - описание термина) задает описание термина и входит в тройку элементов dl, dt, dd, предназначенных для создания списка описаний
---

# &lt;dd&gt;

Тег **`<dd>`** _(от англ. **d**efinition **d**escription - описание термина)_ задает описание термина и входит в тройку элементов `<dl>`, `<dt>`, `<dd>`, предназначенных для создания списка описаний.

Каждый такой список начинается с контейнера [`<dl>`](dl.md), куда входит элемент [`<dt>`](dt.md) создающий термин и элемент `<dd>` задающий описание этого термина.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/dd.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Текстовые блоки"

    <div class="col4" markdown="1">

    - [blockquote](blockquote.md)
    - **dd**
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
<dl>
    <dt>Термин 1</dt>
    <dd>Описание термина 1</dd>
    <dt>Термин 2</dt>
    <dd>Описание термина 2</dd>
</dl>
```

Закрывающий тег не обязателен.

## Атрибуты

Для этого элемента доступны [универсальные атрибуты](uni-attr.md).

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/semantics.html#the-dd-element)
-   [HTML5](http://www.w3.org/TR/html5/grouping-content.html#the-dd-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/lists.html#h-10.3)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>Список описаний</title>
        <style>
            dd {
                font-style: italic; /* Курсивное начертание текста */
            }
            dt {
                margin-top: 1em; /* Отступ сверху */
            }
        </style>
    </head>
    <body>
        <dl>
            <dt>GIF</dt>
            <dd>
                Формат графических файлов, широко
                применяемый при создании сайтов. GIF
                использует 8-битный цвет и эффективно
                сжимает сплошные цветные области, при этом
                сохраняя детали изображения.
            </dd>
            <dt>JPEG</dt>
            <dd>
                Популярный формат графических файлов, широко
                применяемый при создании сайтов и хранения
                изображений. JPEG поддерживает 24-битный
                цвет и сохраняет яркость и оттенки цветов в
                фотографиях. Данный формат называют сжатием
                с потерями, поскольку алгоритм JPEG
                выборочно отвергает данные. Метод сжатия
                может исказить деталь в рисунке, особенно
                содержащий текст или изображение с чёткими
                краями. Формат JPEG не поддерживает
                прозрачность; когда вы сохраняете фотографию
                в формате JPEG, прозрачные пиксели
                заполняются определённым цветом.
            </dd>
        </dl>
    </body>
</html>
```

## Ссылки

-   Тег [`<dd>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/dd) <sup><small>MDN (рус.)</small></sup>
