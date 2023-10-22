---
description: CSS-свойство break-after определяет, как должны вести себя разрывы страницы, столбца или области после сгенерированного блока. Если сгенерированного поля нет, свойство игнорируется.
---

# break-after

Свойство **`break-after`** устанавливает, как должны происходить разрывы страниц, столбцов или областей после сгенерированного блока. Если сгенерированный блок отсутствует, свойство игнорируется.

На каждую возможную точку разрыва (другими словами, на каждую границу элемента) влияют три свойства: значение `break-after` предыдущего элемента, значение `break-before` следующего элемента и значение `break-inside` внутри элемента.

Чтобы определить, должен ли быть сделан разрыв, применяются следующие правила:

1.  Если любое из трех рассматриваемых значений является значением принудительного разрыва (`always`, `left`, `right`, `page`, `column` или `region`), оно имеет приоритет. Если более одного из них является таким разрывом, берется один из элементов, который появляется последним в потоке (т. е. значение `break-before` имеет приоритет над значением `break-after`, которое само по себе имеет приоритет над значением `break-inside`).
2.  Если какое-либо из трех рассматриваемых значений является значением избегания разрыва (`avoid`, `avoid-page`, `avoid-region` или `avoid-column`), такой разрыв не будет применен в этой точке.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/break-after.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Фрагментация"

    <div class="col3" markdown="1">

    - [box-decoration-break](box-decoration-break.md)
    - **break-after**
    - [break-before](break-before.md)
    - [break-inside](break-inside.md)
    - [orphans](orphans.md)
    - [widows](widows.md)

    </div>

## Синтаксис

```css
/* Generic break values */
break-after: auto;
break-after: avoid;
break-after: always;
break-after: all;

/* Page break values */
break-after: avoid-page;
break-after: page;
break-after: left;
break-after: right;
break-after: recto;
break-after: verso;

/* Column break values */
break-after: avoid-column;
break-after: column;

/* Region break values */
break-after: avoid-region;
break-after: region;

/* Global values */
break-after: inherit;
break-after: initial;
break-after: unset;
```

## Значения

Значение по-умолчанию: `auto`

Применяется к блочным элементам.

### Общие значения разрыва

`auto`

: Позволяет, но не заставляет, любой разрыв (страница, столбец или область) вставляться сразу после основного блока.

`avoid`

: Предотвращает вставку любого разрыва (страницы, столбца или региона) сразу после основного блока.

`always`

: Принудительно разрывает страницу сразу после основного окна.

`all`

: Принудительно разрывает страницу сразу после основного окна.

### Значения разрыва страницы

`avoid-page`

: Предотвращает разрыв страницы сразу после основного окна.

`page`

: Принудительно разрывает страницу сразу после основного окна.

`left`

: Принудительно разрывает одну или две страницы сразу после основного окна, в зависимости от того, какая из страниц перейдет на левую страницу.

`right`

: Принудительно разрывает одну или две страницы сразу после основного окна, в зависимости от того, какая из страниц перейдет на нужную страницу.

`recto`

: Принудительно разрывает одну или две страницы сразу после основного окна, в зависимости от того, какая из страниц перейдет на страницу с ректо. (Страница recto - это правая страница в развороте слева направо или левая страница в развороте справа налево.)

`verso`

: Принудительно разрывает одну или две страницы сразу после основного блока, в зависимости от того, какая из страниц превратится в настоящую страницу. (Страница verso - это левая страница в развороте слева направо или слева направо в развороте справа налево.)

### Значения разрыва столбца

`avoid-column`

: Предотвращает разрыв столбца сразу после основного окна.

`column`

: Принудительно разрывает столбец сразу после основного блока.

### Значения границ региона

`avoid-region`

: Позволяет избежать любого разрыва региона сразу после основного блока.

`region`

: Заставляет регион разрываться сразу после основного блока.

### Page break псевдонимы

По причинам совместимости устаревшее свойство [`page-break-after`](page-break-after.md) должно рассматриваться браузерами как псевдоним `break-after`. Это гарантирует, что сайты, использующие разрыв страницы, продолжают работать, как задумано. Подмножество значений должно быть псевдонимом следующим образом:

| `page-break-after` | `break-after` |
| ------------------ | ------------- |
| `auto`             | `auto`        |
| `left`             | `left`        |
| `right`            | `right`       |
| `avoid`            | `avoid`       |
| `always`           | `page`        |

## Спецификации

-   [CSS Fragmentation Module Level 3](https://drafts.csswg.org/css-break-3/#break-between)
-   [CSS Regions Module Level 1](https://drafts.csswg.org/css-regions-1/#region-flow-break)
-   [CSS Multi-column Layout Module](https://drafts.csswg.org/css-multicol-1/#break-before-break-after-break-inside)

## Ссылки

-   [`break-after`](https://developer.mozilla.org/en-US/docs/Web/CSS/break-after) <sup><small>MDN (рус.)</small></sup>
