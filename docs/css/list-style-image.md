---
description: Свойство list-style-image устанавливает адрес изображения, которое служит в качестве маркера списка
---

# list-style-image

Свойство **`list-style-image`** устанавливает адрес изображения, которое служит в качестве маркера списка.

Это свойство наследуется, поэтому для отдельных элементов списка для восстановления маркера используется значение `none`.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/list-style-image.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Списки, счетчики, генерируемый контент"

    <div class="col3" markdown="1">

    - [counter-increment](counter-increment.md)
    - [counter-reset](counter-reset.md)
    - [counter-set](counter-set.md)
    - **list-style-image**
    - [list-style-type](list-style-type.md)
    - [list-style-position](list-style-position.md)
    - [list-style](list-style.md)

    </div>

    <div class="col3" markdown="1">

    - [content](content.md)
    - [quotes](quotes.md)

    </div>

## Синтаксис

```css
/* Keyword values */
list-style-image: none;

/* <url> values */
list-style-image: url('starsolid.gif');

/* Global values */
list-style-image: inherit;
list-style-image: initial;
list-style-image: unset;
```

## Значения

`none`

: Отменяет изображение в качестве маркера для родительского элемента.

`url`

: Относительный или абсолютный путь к графическому файлу. Значение можно указывать в одинарных, двойных кавычках или без них.

Значение по-умолчанию:

```css
list-style-image: none;
```

Применяется к: К элементам [`<dd>`](../html/dd.md), [`<dt>`](../html/dt.md), [`<li>`](../html/li.md), [`<ol>`](../html/ol.md) и [`<ul>`](../html/ul.md), а также ко всем элементам, у которых указано `display: list-item`

## Спецификации

-   [CSS Lists and Counters Module Level 3](http://dev.w3.org/csswg/css3-lists/#list-style-image)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/generate.html#propdef-list-style-image)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>list-style-image</title>
        <style>
            ul {
                list-style-image: url('/example/image/mathematics.png');
            }
        </style>
    </head>
    <body>
        <ul>
            <li>
                Легко проверить, что аффинное преобразование
                монотонно.
            </li>
            <li>
                Доказательство решительно стабилизирует
                отрицательный криволинейный интеграл, явно
                демонстрируя всю чушь вышесказанного.
            </li>
            <li>
                Степенной ряд, в первом приближении,
                расточительно искажает многомерный лист
                Мёбиуса, откуда следует доказываемое
                равенство.
            </li>
        </ul>
    </body>
</html>
```
