---
description: Свойство counter-reset устанавливает переменную, в которой будет храниться счётчик отображений определенного элемента, а также начальное значение счётчика
---

# counter-reset

Свойство **`counter-reset`** устанавливает переменную, в которой будет храниться счётчик отображений определенного элемента, а также начальное значение счётчика.

Такой счётчик может выводиться с помощью свойства [`content`](content.md) и псевдоэлементов `::after` и `::before`.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/counter-reset.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Списки, счетчики, генерируемый контент"

    <div class="col3" markdown="1">

    - [counter-increment](counter-increment.md)
    - **counter-reset**
    - [counter-set](counter-set.md)
    - [list-style-image](list-style-image.md)
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
/* Set "my-counter" to 0 */
counter-reset: my-counter;

/* Set "my-counter" to -1 */
counter-reset: my-counter -1;

/* Set "counter1" to 1, and "counter2" to 4 */
counter-reset: counter1 1 counter2 4;

/* Cancel any reset that could have been set in less specific rules */
counter-reset: none;

/* Global values */
counter-reset: inherit;
counter-reset: initial;
counter-reset: unset;
```

## Значения

`none`

: Запрещает инициацию счётчика для текущего селектора.

`inherit`

: Наследует значение родителя.

`<переменная>`

: Задаёт одну или несколько переменных, в которых будет храниться значение счётчика. Значения разделяются между собой пробелом.

`<число>`

: Начальное значение каждого идентификатора. По умолчанию равно `0`.

### Примечания

Для элементов, у которых установлено `display: none`, значение счётчика не меняется.

Значение по-умолчанию:

```css
counter-reset: none;
```

Применяется ко всем элементам

## Спецификации

-   [CSS Lists and Counters Module Level 3 Рабочий проект](http://dev.w3.org/csswg/css3-lists/#counter-reset)
-   [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/generate.html#propdef-counter-reset)

## Поддержка браузерами

<p class="ciu_embed" data-feature="css-counters" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=css-counters">Can I Use css-counters?</a> Data on support for the css-counters feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>counter-reset</title>
        <style>
            li {
                list-style-type: none;
            } /* Убираем исходную нумерацию у списка */
            ol {
                counter-reset: list1;
            } /* Инициируем счетчик */
            ol li:before {
                counter-increment: list1; /* Увеличиваем значение счетчика */
                content: counter(list1) '. '; /* Выводим число */
            }
            ol ol {
                counter-reset: list2;
            } /* Инициируем счетчик вложенного списка */
            ol ol li:before {
                counter-increment: list2; /* Увеличиваем значение счетчика вложенного списка */
                content: counter(list1) '.' counter(list2)
                    '. '; /* Выводим число */
            }
        </style>
    </head>
    <body>
        <ol>
            <li>
                Пункт
                <ol>
                    <li>Подпункт</li>
                    <li>Подпункт</li>
                    <li>Подпункт</li>
                </ol>
            </li>
            <li>
                Пункт
                <ol>
                    <li>Подпункт</li>
                    <li>Подпункт</li>
                </ol>
            </li>
        </ol>
    </body>
</html>
```
