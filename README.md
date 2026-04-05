# KONTUR Barbershop — GitHub Pages ready

Этот репозиторий подготовлен для деплоя статического сайта через GitHub Pages.

## Что уже сделано

- сайт лежит в папке `docs/`
- все пути переведены на относительные, поэтому сайт работает из подпапки репозитория
- добавлен `.nojekyll`
- добавлен workflow `.github/workflows/deploy-pages.yml`
- Яндекс.Метрика отключена безопасно до указания ID счётчика

## Как задеплоить

1. Создайте GitHub-репозиторий и загрузите в него содержимое этого архива.
2. В GitHub откройте **Settings → Pages**.
3. В разделе **Build and deployment** выберите **Source: GitHub Actions**.
4. Запушьте изменения в ветку `main` или вручную запустите workflow **Deploy static site to GitHub Pages**.

## Что заменить перед продом

### 1) Публичный URL сайта
Откройте `docs/index.html` и задайте:

```html
window.KONTUR_SITE_URL = "https://username.github.io/repo-name/";
```

Если у вас пользовательский домен, укажите его вместо адреса GitHub Pages.

### 2) Яндекс.Метрика
В `docs/index.html` задайте:

```html
window.KONTUR_METRIKA_ID = 12345678;
```

### 3) SEO-файлы
После публикации обновите:

- `docs/robots.txt`
- `docs/sitemap.xml`

там сейчас стоят примерные URL `username.github.io/repo-name`.

## Локальный запуск

```bash
cd docs
python3 -m http.server 8000
```

Откройте `http://localhost:8000`.
