# Путешествие по России

![Путешествие по России](https://im.wampi.ru/2023/05/22/Preview.png)

____

## Описание проекта:

[Путешествие в Россию](https://notacat1.github.io/russian-travel/) - это путешествие в неизвестное. На пути у путешественника возникают большие трудности, которые он должен преодолеть. Но в то же время путешествия в России предоставляет путешественнику много приятных моментов. В данной статье описывается поездка в Россию из Пскова в Улан-Удэ.

____

## Реализованный функционал:

### 1. Favicon

**Favicon** — это иконка, которая отображается во вкладке браузера перед названием сайта.

![Favicon](https://ie.wampi.ru/2023/05/22/imagef7bfc8d5b45cec68.png)

```html
<!-- favicon -->
<link rel="apple-touch-icon" href="./images/favicon/apple-touch-icon.png">
<link rel="icon" href="./images/favicon/favicon.ico" sizes="16x16" type="image/x-icon">
<link rel="manifest" href="./images/favicon/manifest.json">
<link rel="yandex-tableau-widget" href="./images/favicon/tableau.json">
```

### 2. Open Graph

**Open Graph** — это словарь семантической разметки данных. Он позволяет контролировать превью, которое формируется при публикации ссылки на сайт в социальных сетях, и передавать информацию другим интернет-сервисам.

![Open Graph](https://im.wampi.ru/2023/05/22/image9a06a564f10f2b1e.png)

```html
<meta property="og:type" content="website">
<meta property="og:title" content="Путешествия по России">
<meta property="og:description" content="Путешествие в Россию - это путешествие в неизвестное. На пути у путешественника возникают большие трудности, которые он должен преодолеть. Но в то же время путешествия в России предоставляет путешественнику много приятных моментов. В данной статье описывается поездка в Россию из Пскова в Улан-Удэ.">
<meta property="og:url" content="https://github.com/NotACat1">
<meta property="og:image" content="https://im.wampi.ru/2023/05/20/Preview.png">
<meta property="og:site_name" content="NotACat">
<meta property="og:locale" content="ru_RU">
```

### 3. Подключение шрифтов

Одним из способов коммуникации с пользователем является **типографика**. Хороший шрифт на сайте создает настроение, акцентирует внимание человека на важных элементах, его легко читать и он также является отдельным элементом дизайна.

```css
/* Подключение семейство шрифтов Inter */

/* Inter Thin BETA */
@font-face {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 100;
  src: url(./Inter-ThinBETA.woff2) format('woff2'),
       url(./Inter-ThinBETA.woff) format('woff'),
       url(./Inter-ThinBETA.eot) format('eot'),
       url(./Inter-ThinBETA.truetype) format('truetype');
}

/* Inter Thin Italic BETA */
@font-face {
  font-family: 'Inter';
  font-style: italic;
  font-weight: 100;
  src: url(./Inter-ThinItalicBETA.woff2) format('woff2'),
       url(./Inter-ThinItalicBETA.woff) format('woff'),
       url(./Inter-ThinItalicBETA.eot) format('eot'),
       url(./Inter-ThinItalicBETA.truetype) format('truetype');
}

/* Inter Extra Light BETA */
@font-face {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 200;
  src: url(./Inter-ExtraLightBETA.woff2) format('woff2'),
       url(./Inter-ExtraLightBETA.woff) format('woff'),
       url(./Inter-ExtraLightBETA.eot) format('eot'),
       url(./Inter-ExtraLightBETA.truetype) format('truetype');
}
```

### 4. Адапивная верстка

**Адаптивная верстка** — это такой способ создания веб-страниц, при котором они автоматически подстраиваются под размеры и ориентацию экрана устройства, а их дизайн варьируется в зависимости от действий пользователя.

**Цель адаптивной верстки** — добиться того, чтобы сайт оставался удобным и обеспечивал конверсию при загрузке на разных устройствах.

![Малый экран](https://im.wampi.ru/2023/05/22/Small.png)

![Широкий экран](https://ic.wampi.ru/2023/05/22/Grid.png)


### 5. Grid
**Grid (сетка)** — это вид разметки, в котором элементы на сайте расположены в виде таблицы. Главная фишка этой таблицы в гибкости — можно объединять отдельные ячейки, менять размеры строк и столбцов, регулировать отступы между ними. А ещё гриды хорошо приспосабливаются к разным размерам экрана, что делает их адаптивными.

![Grid](https://ic.wampi.ru/2023/05/22/Grid.png)

### 6. Методология БЭМ

**БЭМ (Блок, Элемент, Модификатор)** — компонентный подход к веб-разработке. В его основе лежит принцип разделения интерфейса на независимые блоки. Он позволяет легко и быстро разрабатывать интерфейсы любой сложности и повторно использовать существующий код, избегая «Copy-Paste».

```html
<header class="header">
  <h1 class="header__title">Путешествия по России</h1>
  <p class="header__subtitle">Настоящая страна не в выпусках новостей, а здесь.</p>
  <img class="header__img" src="./images/Route-map.jpg" alt="Маршрут путешествия">
  <p class="header__img-subtitle">ваша полка — верхняя</p>
</header>
```

### 7. Файловая структура Nested

Классическая схема организации файловой структуры БЭМ-проектов:

* Блоку соответствует одна директория.
* Код модификаторов и элементов находится в отдельных файлах.
* Файлы модификаторов и элементов хранятся в отдельных директориях.
* Директория блока является корневой для поддиректорий его элементов и модификаторов.
* Имена директорий элементов начинаются с двойного подчеркивания (__).
* Имена директорий модификаторов начинаются с одинарного подчеркивания (_).

![Файловая структура Nested](https://ic.wampi.ru/2023/05/22/image31fc530f215cfebe.png)

____

## Используемые технологии:
### 1. Normalize.css
Normalize.css позволяет браузерам отображать все элементы более последовательно и в соответствии с современными стандартами. Он точно нацелен только на те стили, которые нуждаются в нормализации.
