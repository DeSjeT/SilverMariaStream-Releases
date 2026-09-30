# Публикация beta-версий

Приложение проверяет публичный файл:

`https://api.github.com/repos/DeSjeT/SilverMariaStream-Releases/contents/beta.json?ref=main`

Файл `beta.json` из этой папки должен находиться в корне публичного репозитория `DeSjeT/SilverMariaStream-Releases`.

- `beta_enabled: false` блокирует запуск всех beta-сборок.
- Более высокая `latest_version` показывает необязательное уведомление об обновлении.
- Более высокая `minimum_supported_version` блокирует устаревшие сборки.
- `download_url` должен вести на опубликованный GitHub Release.
- Текущая схема манифеста: `schema: 1`.

Успешный ответ кэшируется в `%APPDATA%\Silver Maria Stream\beta_manifest_cache.json` на 6 часов. Запрещающий или устаревший кэш блокирует запуск сразу; при отсутствии свежего разрешающего кэша требуется доступ к GitHub.

## Что публиковать

В release-репозитории должны находиться:

- пользовательский `README.md`;
- `TESTER_GUIDE.md`;
- `beta.json`;
- папка `assets` для изображений README;
- ZIP-архивы собранной программы в разделе GitHub Releases.

Не публикуйте исходный проект, `backups`, пользовательские настройки, токены или API-ключи. В beta-архив рядом с `Silver Maria Stream.exe` добавляйте `TESTER_GUIDE.md`.
