# Мета-информация
- это данные о веб-странице, которые не отображаются напрямую пользователям.
- но предоставляют важную информацию для браузеров, поисковых систем, социальных сетей и других сервисов.
- помогает правильно интерпретировать и обрабатывать содержимое страниц, улучшать ее индексирование и обеспечивать правильную работу при шаринге контента.

## Тег `<meta>`
- используется для передачи метаданных, таких как кодировка страницы, описание, ключевые слова и настройки кеширования.
- не имеет закрывающего тега.
- используется только в <head>.

```html
<meta charset="UTF-8">
<meta name="description" content="Описание страницы для поисковых систем">
<meta name="keywords" content="ключевые слова, html, meta теги">
<meta name="author" content="Имя автора">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Основные атрибуты
1. `charset` - задает кодировку символов страницы
2. `name` и `content` - передают мета-данные о странице
    - `description` - краткое описание страницы, которое может использоваться поисковыми системами.
    - `keywords` - ключевые слова для `SEO`(поисковая оптимизация).
    - `author` - автор страницы.
    - `viewport` - отвечает за адаптивную вёрстку, управляя масштабированием страницы на разных устройствах.
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
3. `tp-equiv` - отправляет заголовки HTTP с помощью мета-тега.
    - используется для управления кешированием, перенаправлениями и обновлениями страницы.
    ```html
    <meta http-equiv="refresh" content="30"> <!--  страница будет обновляться каждые 30 с. -->
    ```

## Тег `<title>`
- задает заголовок веб-страницы (заголовок окна браузера, вкладка, результаты поисковых систем)

```html
<title>Мой сайт — Главная страница</title>
```

## Тег `<link>`
- используется для связи HTML-документа с внешними ресурсами (таблицы стилей, фавиконки и др).

```html
<link rel="stylesheet" href="styles.css"> <!-- подключение стилей -->
<link rel="icon" href="favicon.ico" type="image/x-icon"> <!-- добавление фавиконки -->
```

## Тег `<base>`
- задает базовый `url` для всех относительных ссылок на странице.
- если он указан, то все ссылки будут относительно этого `url`.

```html
<!--  все относительные ссылки на странице будут вычисляться относительно этого базового URL -->
<base href="https://example.com/">
```

## Специальные мет-теги для соц.сетей
- помогаю улучшить отображение веб-страницы при ее шаринге в соц.сетях

### Open Graph (OG-теги)
- используются в Facebook  и др. соц.сетях для корректного отображения контента (картинки, описания) при его публикации

```html
<meta property="og:title" content="Название статьи">
<meta property="og:description" content="Описание статьи">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com">
```

### Twitter Cards
- Используются для настройки отображения ссылки в Twitter при ее публикации.

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Название страницы">
<meta name="twitter:description" content="Описание страницы">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

### Пример использования мета-тегов в HTML-документе
```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="Описание вашей страницы для поисковых систем">
    <meta name="keywords" content="ключевые слова, мета-теги, SEO">
    <meta name="author" content="Имя автора">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta property="og:title" content="Название страницы для соцсетей">
    <meta property="og:description" content="Описание страницы для соцсетей">
    <meta property="og:image" content="https://example.com/image.jpg">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Название для Twitter">
    <meta name="twitter:description" content="Описание для Twitter">
    <meta name="twitter:image" content="https://example.com/image.jpg">
    <title>Название страницы</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
    <h1>Основной контент страницы</h1>
</body>
</html>
```