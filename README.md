# KONTUR Barbershop — GitHub Pages

Сайт готов к публикации через GitHub Pages.

## Что уже настроено
- деплой через GitHub Actions
- публикация содержимого папки `docs/`
- относительные пути для CSS, JS, изображений и внутренних ссылок
- `.nojekyll` для корректной раздачи статических файлов

## Как опубликовать
1. Загрузите содержимое этого архива в репозиторий GitHub.
2. Основная ветка должна называться `main`.
3. В GitHub откройте `Settings -> Pages`.
4. В секции `Build and deployment` выберите `GitHub Actions`.
5. Запушьте изменения в `main`.

## Что заменить перед продакшеном
В файлах `docs/*.html`, `docs/robots.txt`, `docs/sitemap.xml` замените:
- `https://username.github.io/repository-name/` на реальный URL Pages
- `REPLACE_WITH_YANDEX_VERIFICATION_CODE` на код верификации Яндекса

Если нужна Яндекс.Метрика, в `docs/index.html` задайте число в строке:
`window.KONTUR_METRIKA_ID = 12345678;`
