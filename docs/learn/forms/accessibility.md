---
description: Как построить инклюзивные формы.
icon: material/wheelchair-accessibility
---

# Доступность

<big>Как построить инклюзивные формы.</big>

Форма, которую вы создаете, предназначена для людей. Люди используют различные устройства. Кто-то использует мышь, кто-то сенсорное устройство, кто-то клавиатуру, кто-то устройство, управляемое движениями глаз. Кто-то пользуется программой чтения с экрана, кто-то - маленьким экраном, кто-то - программой увеличения текста. Все хотят пользоваться вашей формой. Узнайте, как сделать вашу форму доступной и удобной для всех.

## Убедитесь, что пользователи понимают назначение поля формы

Существует множество элементов управления [формы](fields.md), которые можно выбрать. Что их объединяет? Каждый элемент управления формой должен иметь связанный с ним элемент `<label>`. Элемент `<label>` описывает назначение элемента управления формы. Текст `<label>` визуально ассоциируется с элементом управления формы и считывается программами чтения с экрана.

Кроме того, при нажатии или щелчке на элементе `<label>` происходит фокусировка связанного с ним элемента управления формы, что делает его более крупной целью.

!!!note ""

    В следующий раз, добавляя элемент управления формой, сначала добавьте `<label>`. Подумайте о назначении элемента управления формой и опишите его пользователю. Сделайте так, чтобы пользователи могли быстро и точно вводить корректные данные.

## Использование осмысленного HTML для доступа к встроенным функциям браузера

Теоретически можно построить форму, используя только элементы `<div>`. Можно даже сделать ее похожей на родную `<form>`. В чем проблема использования [несемантических](https://developer.mozilla.org/docs/Glossary/Semantics) элементов?

Встроенные элементы формы предоставляют множество встроенных возможностей. Рассмотрим пример.

<iframe src="https://codepen.io/web-dot-dev/embed/2f56a723b5045ea990d38c2c170c3037?height=450&amp;theme-id=light&amp;default-tab=html%2Cresult&amp;editable=true" style="height: 450px; width: 100%; border: 0;" loading="lazy"></iframe>

Визуально `<input>` (первый в примере) и `<div>` выглядят одинаково. Вы даже можете вставить текст для обоих вариантов, поскольку `<div>` имеет атрибут [`contenteditable`](../../html/uni-attr.md#contenteditable). Однако между использованием соответствующего элемента `<input>` и `<div>`, выглядящего как `<input>`, есть много различий.

Пользователь программы чтения с экрана не распознает `<div>` как элемент ввода и не сможет заполнить форму. Все, что слышит пользователь программы чтения с экрана, - это 'Name', без указания на то, что элемент является элементом управления формой для добавления текста.

Щелчок на `<div>Name</div>` не фокусирует связанный с ним `<div>`, тогда как `<label>` и `<input>` связаны между собой атрибутами `for` и `id`.

После отправки формы данные, введенные в `<div>`, не попадают в запрос. Хотя присоединение данных с помощью JavaScript возможно, `<input>` делает это по умолчанию.

Встроенные элементы формы обладают и другими возможностями. Например, при использовании соответствующих элементов формы и правильном `inputmode` или `type` экранная клавиатура отображает соответствующие символы. Использование атрибута `inputmode` на `<div>` не может этого сделать.

## Убедитесь, что пользователи знают о предполагаемом формате данных.

Для элемента управления формой можно определить различные правила валидации. Например, поле формы всегда должно содержать не менее восьми символов. Вы используете атрибут `minlength`, указывая браузеру правило валидации. Как сделать так, чтобы пользователи также знали о правиле валидации? Скажите им.

<iframe src="https://codepen.io/web-dot-dev/embed/b03a4c83688c1b02ab12f9873f1f6614?height=350&amp;theme-id=light&amp;default-tab=html%2Cresult&amp;editable=true" style="height: 350px; width: 100%; border: 0;" loading="lazy"></iframe>

Добавьте информацию об ожидаемом формате непосредственно под элементом управления формой. Чтобы сделать ее понятной для вспомогательных устройств, используйте атрибут `aria-describedby` на элементе управления формой и `id` на сообщении об ошибке с тем же значением, чтобы связать оба элемента.

## Помогите пользователям найти сообщение об ошибке для элемента управления формы

В предыдущем модуле, посвященном [validation](validation.md), вы узнали, как показывать сообщения об ошибках в случае ввода некорректных данных.

```html
<label for="name">Name</label>
<input type="text" name="name" id="name" required />
```

Например, если поле имеет атрибут `required`, и в него введены недопустимые данные, то при отправке формы браузер выводит сообщение об ошибке рядом с элементом управления формой. Программа чтения с экрана также выдает сообщение об ошибке.

Можно также определить собственное сообщение об ошибке:

<iframe src="https://codepen.io/web-dot-dev/embed/b7ed22a0539f9beef4dc03380f51f224?height=300&amp;theme-id=light&amp;default-tab=html%2Cresult&amp;editable=true" style="height: 300px; width: 100%; border: 0;" loading="lazy"></iframe>

Этот пример требует дополнительных изменений, чтобы связать сообщение об ошибке с элементом управления формы.

Простой подход заключается в использовании атрибута `aria-describedby` на элементе управления формой, который соответствует `id` на элементе сообщения об ошибке. Затем использовать [`aria-live="assertive"`](https://developer.mozilla.org/docs/Web/Accessibility/ARIA/ARIA_Live_Regions) для сообщения об ошибке. Области ARIA live сообщают об ошибке пользователям программ чтения с экрана в момент ее отображения.

Проблема такого подхода для форм с несколькими полями заключается в том, что `aria-live` обычно сообщает только о первой ошибке в случае нескольких ошибок. Как объясняется в [этой статье о множественных объявлениях `aria-live` на одно и то же действие](https://gaurav5430.medium.com/quick-accessibility-wins-multiple-aria-live-on-single-action-caveat-b79a6f41e7cc), можно создать единое сообщение, объединив все ошибки. Другой подход заключается в том, чтобы объявить о наличии ошибок, а затем сообщать об отдельных ошибках при фокусировке поля.

## Обеспечить распознавание ошибок пользователями

Иногда дизайнеры окрашивают состояние invalid в красный цвет, используя псевдокласс `:invalid`. Однако, чтобы сообщить об ошибке или успехе, никогда не следует полагаться только на цвет. Для людей с красно-зеленым дальтонизмом зеленая и красная границы выглядят практически одинаково. Невозможно понять, относится ли сообщение к ошибке.

В дополнение к цвету используйте пиктограмму или указывайте в сообщениях об ошибках тип ошибки.

```html
<span class="error">
    <strong>Error:</strong>Please use at least eight
    characters.
</span>
```

## Помощь пользователям в навигации по форме

С помощью CSS можно изменить визуальный порядок элементов управления формы. Несоответствие между визуальным порядком и навигацией по клавиатуре (порядок в DOM) создает проблемы для пользователей программ чтения с экрана и клавиатуры.

Подробнее о том, как обеспечить [визуальный порядок на странице соответствует порядку DOM](https://web.dev/visual-order-follows-dom/).

## Помочь пользователям определить элемент управления формы, на котором они сфокусированы в данный момент.

Используйте клавиатуру для навигации по [этой форме](https://codepen.io/web-dot-dev/pen/c4ab903b77cdfc05dac4707fca69b997). Заметили ли вы, что стиль элементов управления формы изменился, когда они стали активными? Это стиль фокусировки по умолчанию. Вы можете переопределить его с помощью CSS-псевдокласса [`:focus`](../../css/focus.md). Какие бы стили вы ни использовали внутри `:focus`, всегда следите за тем, чтобы визуальная разница между состоянием по умолчанию и состоянием фокуса была заметна.

!!!note ""

    Если необходимо убрать стили по умолчанию `:focus`, но при этом отобразить индикаторы фокуса для пользователей клавиатуры, можно воспользоваться CSS-псевдоклассом [`:focus-visible`](../../css/focus-visible.md).

Подробнее о [разработке индикаторов фокуса](https://www.sarasoueidan.com/blog/focus-indicators/).

## Убедитесь, что ваша форма удобна для использования

Многие типичные проблемы можно выявить, заполняя форму с помощью различных устройств. Используйте только клавиатуру, применяйте программу чтения с экрана (например, [NVDA](https://www.nvaccess.org/) для Windows или [VoiceOver](https://ru.wikipedia.org/wiki/VoiceOver) для Mac) или увеличьте масштаб страницы до 200%. Всегда тестируйте свои формы на разных платформах, особенно на устройствах или настройках, которые вы не используете каждый день. Есть ли у вас знакомые, использующие программу чтения с экрана или программы для увеличения текста? Попросите их заполнить вашу форму. Обзоры доступности - это хорошо, но тестирование с реальными пользователями - еще лучше.

Узнайте больше о том, как сделать [обзор доступности](https://web.dev/how-to-review/) и как провести [тестирование с реальными пользователями](usability-testing.md).

## Ресурсы

-   [WebAIM: Создание доступных форм](https://webaim.org/techniques/forms)
-   [WCAG: преимущества доступности автозаполнения](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html)
-   [Индикаторы фокуса](https://www.sarasoueidan.com/blog/focus-indicators/)

:material-information-outline: Источник &mdash; [Accessibility](https://web.dev/learn/forms/accessibility/)
