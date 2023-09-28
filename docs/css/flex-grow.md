---
description: Свойство flex-grow определяет, сколько пространства может занимать флекс внутри контейнера
---

# flex-grow

Свойство **`flex-grow`** определяет, сколько пространства может занимать флекс внутри контейнера.

В качестве значения принимаются числа, они задают пропорции каждого флекса. К примеру, если для всех элементов установлено значение 1, то они получатся равного размера. Если какой-то элемент получил значение 2, то его размер будет в два раза больше остальных.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/flex-grow.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Flexbox и выравнивание"

    <div class="col3" markdown="1">

    - [flex](flex.md)
    - [flex-basis](flex-basis.md)
    - [flex-direction](flex-direction.md)
    - [flex-flow](flex-flow.md)
    - **flex-grow**
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
/* <number> values */
flex-grow: 3;
flex-grow: 0.6;

/* Global values */
flex-grow: inherit;
flex-grow: initial;
flex-grow: unset;
```

## Значения

Значение по-умолчанию: `0`

Наследуется: нет

Применяется к флекс-элементам

Анимируется: да

`<число>` : Принимаются целые числа. Отрицательные значения игнорируются.

### Примечание

Safari до версии 9 поддерживает свойство `-webkit-flex-grow`.

## Спецификации

-   [CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/#propdef-flex-grow)

## Поддержка браузерами

<p class="ciu_embed" data-feature="flexbox" data-periods="future_1,current,past_1,past_2">
  <a href="http://caniuse.com/#feat=flexbox">Can I Use flexbox?</a> Data on support for the flexbox feature across the major browsers from caniuse.com.
</p>

## Описание и примеры

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>flex-grow</title>
        <style>
            form {
                width: 400px;
                margin: auto;
            }
            p {
                display: flex;
            }
            label {
                margin-right: 10px;
            }
            input,
            select {
                flex-grow: 1;
            }
        </style>
    </head>
    <body>
        <form action="handler.php">
            <p>
                <label>Имя:</label>
                <input name="name" id="name" />
            </p>
            <p>
                <label
                    >Какая у вас операционная
                    система?:</label
                >
                <select name="os">
                    <option value="1">Windows</option>
                    <option value="2">Linux</option>
                    <option value="3">Mac OS</option>
                </select>
            </p>
            <p><button>Отправить</button></p>
        </form>
    </body>
</html>
```

Результат:

<style>
.example form {
width: 400px;
margin: auto;
}
.example p {
display: flex;
}
.example label {
margin-right: 10px;
}
.example input,
.example select {
flex-grow: 1;
}
</style>

<div class="example">
<form action="handler.php">
<p>
<label>Имя:</label>
<input name="name" id="name">
</p>
<p>
<label>Какая у вас операционная система?:</label>
<select name="os">
<option value="1">Windows</option>
<option value="2">Linux</option>
<option value="3">Mac OS</option>
</select>
</p>
<p><button>Отправить</button></p>
</form>
</div>

## См. также

-   [Руководство по Flexbox](../learn/flex/index.md)
