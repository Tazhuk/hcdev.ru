---
description: Свойство isolation определяет, должен ли элемент создать новый контекст стека
---

# isolation

Свойство **`isolation`** определяет, должен ли элемент создать новый контекст стека.

Это особенно полезно в сочетании с [`background-blend-mode`](background-blend-mode.md), которые только смешивают фон в заданном контексте стекирования: он позволяет изолировать группы элементов от их более глубокого фона и смешать их фоновый цвет вместе.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/isolation.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения, фильтры, композиция"

    <div class="col3" markdown="1">

    - [image-orientation](image-orientation.md)
    - [image-rendering](image-rendering.md)
    - [image-resolution](image-resolution.md)
    - [object-fit](object-fit.md)
    - [object-position](object-position.md)

    </div>

    <div class="col3" markdown="1">

    - [linear-gradient()](linear-gradient.md)
    - [radial-gradient()](radial-gradient.md)
    - [repeating-linear-gradient()](repeating-linear-gradient.md)
    - [repeating-radial-gradient()](repeating-radial-gradient.md)
    - [conic-gradient()](conic-gradient.md)
    - [repeating-conic-gradient()](repeating-conic-gradient.md)
    - [url()](url.md)
    - [element()](element.md)
    - [image()](image.md)
    - [cross-fade()](cross-fade.md)

    </div>

    <div class="col3" markdown="1">

    - [backdrop-filter](backdrop-filter.md)
    - [filter](filter.md)

    </div>

    <div class="col3" markdown="1">

    - [background-blend-mode](background-blend-mode.md)
    - **isolation**
    - [mix-blend-mode](mix-blend-mode.md)

    </div>

    <div class="col3" markdown="1">

    - [contain](contain.md)
    - [contain-intrinsic-block-size](contain-intrinsic-block-size.md)
    - [contain-intrinsic-height](contain-intrinsic-height.md)
    - [contain-intrinsic-inline-size](contain-intrinsic-inline-size.md)
    - [contain-intrinsic-size](contain-intrinsic-size.md)
    - [contain-intrinsic-width](contain-intrinsic-width.md)
    - [container](container.md)
    - [container-name](container-name.md)
    - [container-type](container-type.md)
    - [@container](container-at-rule.md)
    - [content-visibility](content-visibility.md)

    </div>

## Синтаксис

```css
/* Keyword values */
isolation: auto;
isolation: isolate;

/* Global values */
isolation: inherit;
isolation: initial;
isolation: unset;
```

## Значения

**`auto`**

: указывает, что новый контекст стека должен быть создан только в том случае, если это требует свойство, применяемое к элементу.

`isolate`

: указывает, что должен быть создан новый контекст стека.

Значение по-умолчанию:

```css
isolation: auto;
```

Применяется ко всем элементам

## Спецификации

-   [Compositing and Blending Level 2](https://drafts.fxtf.org/compositing/#isolation)
-   [Compositing and Blending Level 1](https://drafts.fxtf.org/compositing-1/#isolation)

## Описание и примеры

=== "HTML"

    ```html
    <div id="b" class="a">
      <div id="d">
        <div class="a c">auto</div>
      </div>
      <div id="e">
        <div class="a c">isolate</div>
      </div>
    </div>
    ```

=== "CSS"

    ```css
    .a {
      background-color: rgb(0, 255, 0);
    }
    #b {
      width: 200px;
      height: 210px;
    }
    .c {
      width: 100px;
      height: 100px;
      border: 1px solid black;
      padding: 2px;
      mix-blend-mode: difference;
    }
    #d {
      isolation: auto;
    }
    #e {
      isolation: isolate;
    }
    ```

=== "Результат"

    ![Пример работы свойства isolate](isolate.png)
