# Ход работы

Краткий перечень шагов 1–14 из задания.

| Шаг | Что сделано | Статус |
|---|---|---|
| 1–3 | Python 3.13, venv, каталог проекта | сделано |
| 4 | `requirements.txt` с точными версиями, `.gitignore` | сделано |
| 5–6 | MkDocs Material, `mkdocs build --strict` | сделано |
| 7–8 | Репозиторий и GitHub Actions | workflow подготовлены, запуск за автором |
| 9–10 | Helios или другой хостинг | _TODO_ |
| 11 | `site_url`, `use_directory_urls` | настроено, проверить после публикации |
| 12 | Проверка HTTP-кода и поиска | шаг healthcheck есть в workflow |
| 13 | Лицензии: MIT и CC BY 4.0 | сделано |
| 14 | Отладка | см. [Отладка](debug.md) |

## Pages: два подхода

- `peaceiris/actions-gh-pages` пушит собранный сайт в ветку `gh-pages`; нужен токен с правом записи в репозиторий.
- `actions/upload-pages-artifact` + `actions/deploy-pages` публикуют артефакт напрямую, права ограничены `pages: write` и `id-token: write`, ветка с HTML не нужна. Выбран этот вариант.
