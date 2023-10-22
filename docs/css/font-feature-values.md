---
description: Правило @font-feature-values позволяет использовать общее имя в свойстве font-variant-alternates для функций, которые по разному активируются в OpenType
---

# @font-feature-values

Правило **`@font-feature-values`** позволяет использовать общее имя в свойстве `font-variant-alternates` для функций, которые по разному активируются в OpenType. Это может помочь упростить ваш CSS при использовании нескольких шрифтов.

Правило `@font-feature-values` может использоваться как на вернем уровне вашего CSS так и внутри любого условного CSS правила.

??? info "@-правила"

    <div class="col3" markdown="1">

    - [@charset](charset.md)
    - [@import](import.md)
    - [@namespace](namespace.md)
    - [@media](media.md)
    - [@supports](supports.md)
    - [@document](document.md)
    - [@page](page.md)
    - [@font-face](font-face.md)
    - [@keyframes](keyframes.md)
    - [@viewport](viewport.md)
    - [@counter-style](counter-style.md)
    - **@font-feature-values**

    </div>

## Синтаксис

```css
/* Правило для "хорошего стиля" в Font One */
@font-feature-values Font One {
    @styleset {
        nice-style: 12;
    }
}

/* Правило для "хорошего стиля" в Font Two */
@font-feature-values Font Two {
    @styleset {
        nice-style: 4;
    }
}

/* Применение правилоа с единственым объявлением */
.nice-look {
    font-variant-alternates: styleset(nice-style);
}
```

## Значения

`@swash`

: Устанавливает имя функции, которая будет работать с функциональной записью `swash()` для `font-variant-alternates`. Определение значения функции `swash` допускает только одно значение: `ident1: 2` является действительным, но `ident2: 2 4` нет.

`@annotation`

: Устанавливает имя фунции, которая будет работать с функциональной записью `annotation()` для `font-variant-alternates`. Определение значения функции допускает только одно значение: `ident1: 2` действительным , но `ident2: 2 4` нет.

`@ornaments`

: Устанавливает имя функции, которая будет работать с функциональной записью `ornaments()` для `font-variant-alternates`. Определение значения функции `ornaments` допускает только одно значение: `ident1: 2` является действительным, но `ident2: 2 4` нет.

`@stylistic`

: Задает имя функции, которая будет работать с функциональной нотацией `stylistic()` `font-option-alternates`. Определение значения стилистического признака допускает только одно значение: `ident1: 2` является действительным, а `identif2: 2 4` - нет.

`@styleset`

: Указывает имя функции, которая будет работать с функциональной нотацией `styleset()` `font-option-alternates`. Определение значения функции стилета допускает неограниченное количество значений: `identif1: 2 4 12 1` сопоставляется со значениями OpenType `ss02`, `ss04`, `ss12` и `ss01`. Обратите внимание, что значения выше 99 действительны, но не отображаются ни на какие значения OpenType и игнорируются.

`@character-variant`

: Задает имя функции, которая будет работать с функциональной нотацией `character-variant()` `font-variant-alternates`. Определение значения признака в символьном варианте допускает одно или два значения: `ident1: 3` сопоставляется с `cv03 = 1`, а `symb2: 2 4` сопоставляется с `cv02 = 4`, но `ident2: 2 4 5` недопустимо.

## Спецификация

-   [CSS Fonts Module Level 3](https://drafts.csswg.org/css-fonts-3/#font-feature-values)

## См. также

-   Свойство `font-variant-alternates` которое использует значения, определенные этим правилом.

## Ссылки

-   [`font-variant-alternates`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant-alternates) <sup><small>MDN (рус.)</small></sup>
