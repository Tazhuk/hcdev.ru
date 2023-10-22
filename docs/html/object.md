---
description: Тег object (от англ. object — объект) сообщает браузеру, как загружать и отображать объекты, которые исходно браузер не понимает
---

# &lt;object&gt;

Тег **`<object>`** _(от англ. **object** — объект)_ сообщает браузеру, как загружать и отображать объекты, которые исходно браузер не понимает.

Как правило, такие объекты требуют подключения к браузеру специального модуля, который называется плагин, или запуска вспомогательной программы.

Дополнительно внутрь контейнера `<object>` можно поместить элемент [`<param>`](param.md), который передаёт дополнительные параметры для отображения объекта.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/object.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

??? info "Изображения и мультимедиа"

    <div class="col4" markdown="1">

    - [area](area.md)
    - [audio](audio.md)
    - [img](img.md)
    - [figcaption](figcaption.md)
    - [figure](figure.md)
    - [map](map.md)
    - [track](track.md)
    - [video](video.md)
    - [embed](embed.md)
    - [iframe](iframe.md)
    - **object**
    - [param](param.md)
    - [picture](picture.md)
    - [source](source.md)

    </div>

## Синтаксис

```html
<object></object>
```

Закрывающий тег обязателен.

## Атрибуты

[`data`](#data)

: Адрес файла для его отображения в окне браузера.

[`height`](#height-width)

: Высота объекта.

[`type`](#type)

: MIME-тип объекта.

[`width`](#height-width)

: Ширина объекта.

Также для этого элемента доступны [универсальные атрибуты](uni-attr.md).

### data

Определяет файл, который следует отобразить в окне браузера. Для популярных форматов данных достаточно указать путь к файлу и его тип (атрибут `type`) для загрузки и демонстрации результата.

Путь следует задавать относительно текущего документа.

**Синтаксис**

```html
<object data="<адрес>">...</object>
```

**Значения**

В качестве значения принимается полный или относительный путь к файлу.

**Значение по умолчанию**

Нет.

### height и width {#height-width}

Атрибут `height` устанавливает высоту объекта, а `width` — его ширину. В заданные размеры входит не только само изображение, например в случае воспроизведения видеофайла, но и панель управления им, включая кнопки проигрывания, паузы, остановки и т. д. По этой причине на размер отображаемого объекта влияет тип файла и применяемый плагин.

Если используется процентная запись, то размеры объекта вычисляются относительно родительского элемента — контейнера, где находится элемент `<object>`. В случае отсутствия родительского контейнера, в его качестве выступает окно браузера. Иными словами, `width="100%"` означает, что объект будет занимать всю доступную ширину веб-страницы.

**Синтаксис**

```html
<object height="значение" width="значение">...</object>
```

**Значения**

Любое целое положительное число в пикселях или процентах.

**Значение по умолчанию**

Нет.

### type

Устанавливает MIME-тип объекта для распознавания браузером.

**Синтаксис**

```html
<object type="<MIME-тип>">...</object>
```

**Значения**

Имя MIME-типа в любом регистре.

**Значение по умолчанию**

Нет.

## Спецификации

-   [HTML Living Standard](https://html.spec.whatwg.org/multipage/embedded-content.html#the-object-element)
-   [HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-object-element)
-   [HTML 4.01 Specification](http://www.w3.org/TR/html401/struct/objects.html#h-13.3)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>OBJECT</title>
    </head>
    <body>
        <p>
            <object
                type="application/x-shockwave-flash"
                data="flash/mouse.swf"
                width="400"
                height="300"
            >
                <param name="quality" value="high" />
                <param name="wmode" value="opaque" />
            </object>
        </p>
    </body>
</html>
```

## Ссылки

-   Тег [`<object>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/object) <sup><small>MDN (рус.)</small></sup>
