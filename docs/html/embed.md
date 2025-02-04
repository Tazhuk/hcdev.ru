---
description: Тег embed (от англ. embed - встраивать) используется для загрузки и отображения объектов, которые исходно браузер не понимает
---

# &lt;embed&gt;

Тег **`<embed>`** _(от англ. **embed** - встраивать)_ используется для загрузки и отображения объектов (например, видеофайлов, флэш-роликов, некоторых звуковых файлов и т. д.), которые исходно браузер не понимает.

Как правило, такие объекты требуют подключения к браузеру специального модуля, который называется плагин, или запуска вспомогательной программы. Вид внедрённого объекта зависит от установленных в браузере плагинов, типа загружаемого файла, а также от атрибутов элемента `<embed>`.

## Демо

<iframe class="interactive is-tabbed-standard-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/tabbed/embed.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

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
    - **embed**
    - [iframe](iframe.md)
    - [object](object.md)
    - [param](param.md)
    - [picture](picture.md)
    - [source](source.md)

    </div>

## Синтаксис

```html
<embed></embed>
```

Закрывающий тег не требуется.

## Атрибуты

[`height`](#height)

: Высота объекта.

[`hidden`](#hidden)

: Указывает, скрыть объект на странице или нет.

[`pluginspage`](#pluginspage)

: Адрес страницы в Интернете, откуда можно скачать и установить плагин к браузеру.

[`src`](#src)

: Путь к файлу.

[`type`](#type)

: MIME-тип объекта.

[`width`](#width)

: Ширина объекта.

### height

Атрибут `height` устанавливает высоту объекта. В заданные размеры входит не только само изображение, например в случае воспроизведения видеофайла, но и панель управления им, включая кнопки проигрывания, паузы, остановки и т. д. По этой причине на размер отображаемого объекта влияет тип файла и применяемый плагин.

Если используется процентная запись, то размеры объекта вычисляются относительно родительского элемента — контейнера, где располагается элемент `<embed>`. В случае отсутствия родительского контейнера, в его качестве выступает окно браузера. Иными словами, `height="100%"` означает, что объект будет занимать всю доступную высоту веб-страницы.

**Синтаксис**

```html
<embed height="<значение>">
	...
</embed>
```

**Значения**

Любое целое положительное число в пикселях или процентах.

**Значение по умолчанию**

Нет.

### hidden

Атрибут `hidden` представляет собой выключатель, который определяет, отображать объект в окне браузера или нет. Это особенно удобно для скрытия панели управления при воспроизведении фоновой музыки. Если этот атрибут указан, то значения атрибутов `width` и `height` игнорируются.

**Синтаксис**

```html
<embed hidden="true | false">...</embed>
```

**Значения**

`true`

: Скрывает объект.

`false`

: Отображает объект на странице.

**Значение по умолчанию**

-   `false`

### pluginspage

Если браузер не поддерживает указанный тип файлов заданный атрибутом `src`, то `pluginspage` используется для того, чтобы перейти по указанному адресу, откуда можно скачать и установить необходимый плагин. Браузер сообщает пользователю, что требуемого плагина для отображения файла нет, и запрашивает, загружать его или нет.

**Синтаксис**

```html
<embed pluginspage="адрес">...</embed>
```

**Значения**

Любой корректный адрес, ведущий на веб-страницу с плагином.

**Значение по умолчанию**

Нет.

### src

Атрибут `src` указывает путь к файлу, который необходимо загрузить в окно браузера. Браузер анализирует расширение файла и решает по нему, какой плагин или внешняя программа требуется для отображения файла.

**Синтаксис**

```html
<embed src="<адрес>">...</embed>
```

**Значения**

В качестве значения принимается полный или относительный путь к файлу.

**Значение по умолчанию**

Нет.

### type

Не всегда браузер может распознать тип файла по его расширению. В таких случаях лучше указывать его тип с помощью атрибута `type`, который устанавливает MIME-тип для данных.

**Синтаксис**

```html
<embed type="<MIME-тип>">...</embed>
```

**Значения**

Имя MIME-типа в любом регистре. Допускается устанавливать сразу несколько значений, разделяя их запятыми.

**Значение по умолчанию**

Нет.

### width

Атрибут `width` устанавливает ширину объекта. В заданные размеры входит не только само изображение, например в случае воспроизведения видеофайла, но и панель управления им, включая кнопки проигрывания, паузы, остановки и т. д. По этой причине на размер отображаемого объекта влияет тип файла и применяемый плагин.

Если используется процентная запись, то размеры объекта вычисляются относительно родительского элемента — контейнера, где находится элемент `<embed>`. В случае отсутствия родительского контейнера, в его качестве выступает окно браузера. Иными словами, `width="100%"` означает, что объект будет занимать всю доступную ширину веб-страницы.

**Синтаксис**

```html
<embed width="значение">
	...
</embed>
```

**Значения**

Любое целое положительное число в пикселях или процентах.

**Значение по умолчанию**

Нет.

## Спецификации

-   [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/embedded-content.html#the-embed-element)
-   [HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-embed-element)

## Описание и примеры

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>EMBED</title>
    </head>
    <body>
        <embed
            src="flash/mouse.swf"
            width="400"
            height="300"
            type="application/x-shockwave-flash"
            pluginspage="https://get.adobe.com/flashplayer"
        />
    </body>
</html>
```

## Ссылки

-   Тег [`<embed>`](https://developer.mozilla.org/ru/docs/Web/HTML/Element/embed) <sup><small>MDN (рус.)</small></sup>
