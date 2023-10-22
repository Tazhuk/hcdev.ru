---
description: Свойство border-image используется для отображения рисованной рамки вокруг элемента
---

# border-image

Свойство **`border-image`** используется для отображения рисованной рамки вокруг элемента.

Толщина рамки задаётся свойством [`border`](border.md), при этом если указано `border: 0`, то рамка не выводится. При других значениях `border` рисунок всегда имеет приоритет. Фон, если он задан через свойство [`background`](background.md), отображается под рамкой.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/border-image.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

Это свойство является сокращением для следующих свойств CSS:

-   `border-image-outset`
-   `border-image-repeat`
-   `border-image-slice`
-   `border-image-source`
-   `border-image-width`

??? info "Фон"

    <div class="col3" markdown="1">

    - [border](border.md)
    - [border-bottom](border-bottom.md)
    - [border-bottom-color](border-bottom-color.md)
    - [border-bottom-left-radius](border-bottom-left-radius.md)
    - [border-bottom-right-radius](border-bottom-right-radius.md)
    - [border-bottom-style](border-bottom-style.md)
    - [border-bottom-width](border-bottom-width.md)
    - [border-collapse](border-collapse.md)
    - [border-color](border-color.md)
    - **border-image**
    - [border-image-outset](border-image-outset.md)
    - [border-image-repeat](border-image-repeat.md)
    - [border-image-slice](border-image-slice.md)
    - [border-image-source](border-image-source.md)
    - [border-image-width](border-image-width.md)
    - [border-left](border-left.md)
    - [border-left-color](border-left-color.md)
    - [border-left-style](border-left-style.md)
    - [border-left-width](border-left-width.md)
    - [border-radius](border-radius.md)
    - [border-right](border-right.md)
    - [border-right-color](border-right-color.md)
    - [border-right-style](border-right-style.md)
    - [border-right-width](border-right-width.md)
    - [border-style](border-style.md)
    - [border-top](border-top.md)
    - [border-top-color](border-top-color.md)
    - [border-top-left-radius](border-top-left-radius.md)
    - [border-top-right-radius](border-top-right-radius.md)
    - [border-top-style](border-top-style.md)
    - [border-top-width](border-top-width.md)
    - [border-width](border-width.md)
    - [box-shadow](box-shadow.md)

    </div>

## Синтаксис

```css
/* source | slice */
border-image: linear-gradient(red, blue) 27;

/* source | slice | repeat */
border-image: url('/images/border.png') 27 space;

/* source | slice | width */
border-image: linear-gradient(red, blue) 27 / 35px;

/* source | slice | width | outset | repeat */
border-image: url('/images/border.png') 27 23 / 50px 30px /
    1rem round space;

/* Global values */
border-image: inherit;
border-image: initial;
border-image: revert;
border-image: revert-layer;
border-image: unset;
```

Для свойства `border-image` может быть указано от одного до пяти значений, перечисленных ниже.

## Значения

`none`

: Не отображает рисованную рамку, используется установленный стиль границы.

`URL`

: Путь к графическому файлу. Обязательный параметр.

Само изображение для создания рамки продемонстрировано на рис. 1 и состоит из девяти областей: четырёх уголков, верхней, правой, нижней, левой стороны и центральной части, в которой выводится содержимое элемента.

![Рис. 1. Изображение для создания рамки](css_border-image-1.png)

`<число>`

: Одно, два, три или четыре значения, которые указывают размеры частей изображения в пикселях, задавая тем самым области деления. Сами единицы не пишутся, только число (10, а не 10px).На рис. 2 красными линиями выделены необходимые для создания рамки области.

![Рис. 2. Деление исходного изображения на области](css_border-image-2.png)

Разрешается использовать одно, два, три или четыре значения, разделяя их между собой пробелом. Эффект зависит от количества значений и приведен в табл. 1.

<table>
<caption>Табл. 1. Зависимость от числа значений</caption>
<thead>
<tr><th>Число значений</th><th>Результат</th></tr>
</thead>
<tbody>
<tr><td>1</td><td>Устанавливает границы одинаковой толщины на каждой стороне рисунка.</td></tr>
<tr><td>2</td><td>Первое значение устанавливает высоту верхней и нижней границы, второе — левой и правой.</td></tr>
<tr><td>3</td><td>Первое значение определяет высоту верхней границы, второе — левой и правой, а третье — высоту нижней границы.</td></tr>
<tr><td>4</td><td>Поочерёдно устанавливается размеры верхней, правой, нижней и левой границы.</td></tr>
</tbody>
</table>

`<проценты>`

: Аналогично `<числу>`, но значения задаются в процентах. Тот или другой параметр обязателен.

`<толщина>`

: Через слэш пишется одно, два, три или четыре значения толщины границы на каждой стороне элемента. Является аналогом [`border-width`](border-width.md) и использует тот же синтаксис.

`stretch`

: Растягивает рисунок границы до размеров элемента. Это значение используется по умолчанию.

`repeat`

: Повторяет рисунок границы.

`round`

: Повторяет рисунок и масштабирует его так, чтобы на стороне элемента оказалось целое число изображений.

Влияние этих параметров на вид рамки показано на рисунках.

![Рамка с параметром stretch](css_border-image-3a.png)

![Рамка с параметром repeat](css_border-image-3b.png)

![Рамка с параметром round](css_border-image-3c.png)

Значение по-умолчанию:

```css
border-image: none;
```

Применяется ко всем элементам, за исключением тех, у кого [`border-collapse`](border-collapse.md) задан как `collapse`

## Спецификации

-   [CSS Backgrounds and Borders Module Level 3](https://w3c.github.io/csswg-drafts/css-backgrounds/#the-border-image)

## Поддержка браузерами

<p class="ciu_embed" data-feature="border-image" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=border-image">Can I Use border-image?</a> Data on support for the border-image feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>border-image</title>
        <style>
            div {
                border: 30px solid #40c4c8;
                padding: 20px;
                border-image: url(/example/image/bg-image.png)
                    30 round round;
            }
        </style>
    </head>
    <body>
        <div>
            Витраж представляет собой композицию сделанную
            из множества цветных стекол обрамлённых
            проволокой и наиболее эффектно смотрится при
            прохождении через него солнечного или
            искусственного света.
        </div>
    </body>
</html>
```

### Ссылки

-   [генератор кода border-image](https://border-image.com/)
