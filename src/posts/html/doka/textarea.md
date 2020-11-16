---
title: <textarea>
name: textarea
autor: ezhkov_d
co-autors:
designers:
contributors:
summary:
  - поле ввода многострочного текста
  - элемент формы
---

## Кратко

Тег `<textarea>` используется для создания многострочного поля ввода. Например, поля ввода комментария. При необходимости поле может иметь изменяемый размер.

## Пример

```html
<label for="story">Расскажите о себе:</label>
<textarea id="story" name="story" rows="5" cols="33">
  Frontend-разработчик со стажем
</textarea>
```

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="eYzgwgN" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/eYzgwgN">
  &lt;textarea&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Как это понять

На сайтах часто встречаются формы, где нужно писать многострочный текст. Например, когда нужно оставить комментарий, написать отзыв или статью. Для этих целей используется многострочное поле ввода, которое верстается тегом `<textarea>`. Нужно отметить, что в этом поле можно писать только чистый текст, то есть панели стилизации текста, как в Ворде, это дополнительные надстройки с использованием Javascript

## Атрибуты

### `autocomplete`

Атрибут, указывающий, нужно ли поле заполнять автоматически сохраненными в браузере значениями. Полезно использовать, если одна и та же форма потенциально будет часто отправляться с одинаковыми значениями.

Значения атрибута:

`on` — поле будет автоматически заполняться значением, сохраненным в браузере во время предыдущей отправки формы

`off` — поле не будет заполняться браузером автоматически. Также, это значение нужно использовать, если документ предоставляет собственный метод автозаполнения полей.

Если атрибут не указать совсем, то браузер будет брать значение из атрибута `autocomplete` родительского элемента [&lt;form>](/posts/html/doka/form), либо — если родительской формы нет — из той формы, на `id` которой ссылается атрибуте `form`.

```html
<textarea autocomplete="off"></textarea>
```

### `autofocus`

Атрибут булевого типа (без значения, либо атрибут есть в теге, либо его нет совсем). Если он указан, то при загрузке страницы фокус будет автоматически помещён в данное поле ввода.

```html
<textarea autofocus></textarea>
```

### `cols`

Задаёт ширину поля ввода в символах. Если атрибут задан, то должен иметь значением целое положительное число. Если не задан, то по умолчанию берётся как 20

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="YzWNojL" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea cols&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/YzWNojL">
  &lt;textarea cols&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

### `disabled`

Атрибут булевого типа. Если задан, то поле отключается для взаимодействия с пользователем. Если атрибут не задан, то он может быть унаследован у одного из предков (например у контейнера &lt;fieldset> или [&lt;form>](/posts/html/doka/form). Если ни у одного предка вверх по дереву этот атрибут не задан, то поле доступно для редактирования.

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="eYzgwqg" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/eYzgwqg">
  &lt;textarea&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

При отправке формы значения из disabled-полей не будут отправлены

### `form`

Атрибут указывает на элемент [&lt;form>](/posts/html/doka/form), с которым связано поле ввода. Значением атрибута должен быть `id` формы в пределах текущего документа. Если атрибут не задан, то `<textarea>` обязательно должен находиться внутри тега [&lt;form>](/posts/html/doka/form). Но если задать атрибут, то нахождение внутри формы не обязательно и `<textarea>` может находиться в любом месте страницы.

### `maxlength`

Максимальное число символов в поле (включая пробелы и переводы строк), которое может вводить пользователь. Значением должно быть положительное целое число

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="jOrygOb" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea maxlength&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/jOrygOb">
  &lt;textarea maxlength&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

### `minlength`

Минимальное число символов, которое должен ввести пользователь. Этот атрибут используется при валидации поля перед отправкой формы.

### `name`

Имя поля. При отправке формы значение атрибута `name` будет ключом в отправляемом объекте

### `placeholder`

Подсказка для пользователя, что вводить в этом поле. Если подсказка должна быть многострочной, то можно прямо в HTML-коде переносить строки

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="jOrygBM" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea placeholder&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/jOrygBM">
  &lt;textarea placeholder&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Плейсхолдер должен давать только подсказку о том, как должно заполняться поле. Но это не полноценная замена тегу [&lt;label>](/posts/html/doka/label). Если на дизайне у полей ввода есть только плейсхолдер, но нет лейблов, рекомендуется вернуть дизайн в доработку 😉

### `readonly`

Атрибут булевого типа. Если он задан, то пользователь не может редактировать текст в поле, но по-прежнему может с ним взаимодействовать: кликать, копировать текст. При отправке формы значение поля будет отправлено как обычно.

### `required`

Атрибут булевого типа. Указывает, должно ли поле обязательно быть заполнено. Атрибут учитывается при валидации формы при отправке. Если поле не заполнить, то при попытке отправки формы браузер покажет ошибку

### `rows`

Задаёт высоту поля ввода в строках. Если атрибут задан, то должен иметь значением целое положительное число. Если не задан, то по умолчанию высота задается равной двум строкам.

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="result" data-user="ezhkov" data-slug-hash="xxOrZGR" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;textarea rows&amp;gt;">
  <span>See the Pen <a href="https://codepen.io/ezhkov/pen/xxOrZGR">
  &lt;textarea rows&gt;</a> by Denis Ezhkov (<a href="https://codepen.io/ezhkov">@ezhkov</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

### `spellcheck`

Атрибут указывает, должна ли быть включена проверка правописания в поле. Может принимать следующие значения:

`true` — проверка правописания включена

`default` — указывает на поведение по умолчанию. При этом значении поле ввода может наследовать значение аналогичного атрибута от родительских элементов.

`false` — проверка правописания выключена

### `wrap`

Атрибут определяет, будут ли добавлены символы переноса строк текста при отправке формы. Может принимать значения:

`hard` — когда форма отправляется, то браузер, основываясь на значении атрибута `cols` добавляет в текст служебные символы переноса строки (CR+LF). Таким образом, сохраняется информация о переносах строк, сделанных пользователем в поле ввода.

`soft` — значение по умолчанию. При отправке формы символы переноса строк добавлены не будут, и текст будет отправлен одной длинной строкой

## Подсказки

💡Поле `<textarea>` стилизуется так же, как и поле ввода [&lt;input>](/posts/html/doka/input). К нему применимы все свойства блочной модели.

💡По умолчанию поле ввода `<textarea>` может изменять свой размер, если потянуть за нижний правый угол. Это поведение можно изменить, управляя CSS-свойством resize.

{% include "autors/ezhkov_d/autor.njk" %}