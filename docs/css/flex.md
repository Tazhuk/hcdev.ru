---
description: Сокращённое свойство flex, которое позволяет указать параметры элемента, чтобы он эффективно заполнял доступное пространство
---

# flex

Сокращённое свойство **`flex`**, которое позволяет указать параметры элемента, чтобы он эффективно заполнял доступное пространство.

Элементы могут быть растянуты пропорционально с учётом заданного соотношения или сжаты, чтобы целиком вместить все элементы без переносов в одну строку.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/flex.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Flexbox и выравнивание"

    <div class="col3" markdown="1">

    - **flex**
    - [flex-basis](flex-basis.md)
    - [flex-direction](flex-direction.md)
    - [flex-flow](flex-flow.md)
    - [flex-grow](flex-grow.md)
    - [flex-shrink](flex-shrink.md)
    - [flex-wrap](flex-wrap.md)
    - [order](order.md)

    </div>

    <div class="col3" markdown="1">

    - [justify-content](justify-content.md)
    - [align-content](align-content.md)
    - [place-content](place-content.md)
    - [justify-items](justify-items.md)
    - [align-items](align-items.md)
    - [place-items](place-items.md)
    - [justify-self](justify-self.md)
    - [align-self](align-self.md)
    - [place-self](place-self.md)
    - [row-gap](row-gap.md)
    - [column-gap](column-gap.md)
    - [gap](gap.md)

    </div>

## Синтаксис

```css
/* Basic values */
flex: auto;
flex: initial;
flex: none;
flex: 2;

/* One value, unitless number: flex-grow */
flex: 2;

/* One value, width/height: flex-basis */
flex: 10em;
flex: 30px;

/* Two values: flex-grow | flex-basis */
flex: 1 30px;

/* Two values: flex-grow | flex-shrink */
flex: 2 2;

/* Three values: flex-grow | flex-shrink | flex-basis */
flex: 2 2 10%;

/* Global values */
flex: inherit;
flex: initial;
flex: unset;
```

## Значения

Значение по-умолчанию:

-   [`flex-grow`](flex-grow.md): `0`
-   [`flex-shrink`](flex-shrink.md): `1`
-   [`flex-basis`](flex-basis.md): `auto`

Наследуется: нет

Применяется к флекс-элементам

Анимируется: да

`none`

: Соответствует значению `0 0 auto`.

!!! note "Примечание"

    Safari до версии 9 поддерживает свойство `-webkit-flex`.

## Спецификации

-   [CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/#flex-property)

## Поддержка браузерами

<p class="ciu_embed" data-feature="flexbox" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=flexbox">Can I Use flexbox?</a> Data on support for the flexbox feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

CSS

```css
#flex-container {
    display: flex;
    flex-direction: row;
}

#flex-container > .flex-item {
    flex: auto;
}

#flex-container > .raw-item {
    width: 5rem;
}
```

HTML

```html
<div id="flex-container">
    <div class="flex-item" id="flex">
        Flex box (click to toggle raw box)
    </div>
    <div class="raw-item" id="raw">Raw box</div>
</div>
```

Результат

![Результат работы свойства flex](flex.png)

## См. также

-   [Руководство по Flexbox](../learn/flex/index.md)
