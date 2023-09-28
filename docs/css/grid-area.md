---
description: Свойство grid-area даёт название элементу чтобы можно было ссылаться на него с помощью шаблона созданного через grid-template-areas свойство
---

# grid-area

Свойство **`grid-area`** даёт название элементу чтобы можно было ссылаться на него с помощью шаблона созданного через [`grid-template-areas`](grid-template-areas.md) свойство.

Свойство **`grid-area`** является сокращенным свойством для [`grid-row-start`](grid-row-start.md), [`grid-column-start`](grid-column-start.md), [`grid-row-end`](grid-row-end.md) и [`grid-column-end`](grid-column-end.md), определяя размер и расположение элемента сетки.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/grid-area.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Grid Layout"

    <div class="col3" markdown="1">

    - [grid](grid.md)
    - **grid-area**
    - [grid-auto-columns](grid-auto-columns.md)
    - [grid-auto-flow](grid-auto-flow.md)
    - [grid-auto-rows](grid-auto-rows.md)
    - [grid-column](grid-column.md)
    - [grid-column-end](grid-column-end.md)
    - [grid-column-gap](grid-column-gap.md)
    - [grid-column-start](grid-column-start.md)
    - [grid-gap](grid-gap.md)
    - [grid-row](grid-row.md)
    - [grid-row-end](grid-row-end.md)
    - [grid-row-gap](grid-row-gap.md)
    - [grid-row-start](grid-row-start.md)
    - [grid-template](grid-template.md)
    - [grid-template-areas](grid-template-areas.md)
    - [grid-template-columns](grid-template-columns.md)
    - [grid-template-rows](grid-template-rows.md)

    </div>

## Синтаксис

```css
/* Keyword values */
grid-area: auto;
grid-area: auto / auto;
grid-area: auto / auto / auto;
grid-area: auto / auto / auto / auto;

/* <custom-ident> values */
grid-area: some-grid-area;
grid-area: some-grid-area / another-grid-area;

/* <integer> && <custom-ident>? values */
grid-area: some-grid-area 4;
grid-area: some-grid-area 4 / 2 another-grid-area;

/* span && [ <integer> || <custom-ident> ] values */
grid-area: span 3;
grid-area: span 3 / span some-grid-area;
grid-area: 2 span / another-grid-area span;

/* Global values */
grid-area: inherit;
grid-area: initial;
grid-area: unset;
```

## Значения

Значение по-умолчанию:

-   `grid-row-start: auto`
-   `grid-column-start: auto`
-   `grid-row-end: auto`
-   `grid-column-end: auto`

Наследуется: нет

Применяется к элементам сетки

Анимируется: нет

Объектная модель: `object.style.gridArea`

## Спецификации

-   [CSS Grid Layout](https://drafts.csswg.org/css-grid/#propdef-grid-area)

## Поддержка браузерами

<p class="ciu_embed" data-feature="css-grid" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=css-grid">Can I Use css-grid?</a> Data on support for the css-grid feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

=== "HTML"

    ```html
    <div id="grid">
    	<div id="item1"></div>
    	<div id="item2"></div>
    	<div id="item3"></div>
    </div>
    ```

=== "CSS"

    ```css
    #grid {
    	display: grid;
    	height: 100px;
    	grid-template: repeat(4, 1fr) / 50px 100px;
    }

    #item1 {
    	background-color: lime;
    	grid-area: 2 / 2 / auto / span 3;
    }

    #item2 {
    	background-color: yellow;
    }

    #item3 {
    	background-color: blue;
    }
    ```

=== "Результат"

    ![Пример использования свойства grid-area](grid-area.png)

## См. также

-   [Руководство по Grid Layout](../learn/grid/index.md)
