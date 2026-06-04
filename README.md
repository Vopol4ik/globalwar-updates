# Project Global Conflict — обновления для лаунчера

Сюда попадает **только** `modpack-manifest.json` (список файлов и SHA).

Сами jar/zip лежат в **GitHub Releases** (тег `modpack-latest`), чтобы не раздувать git.

## Публикация обновления

1. В `launcher/src/config.js` укажите `github.owner` и `github.repo`.
2. Создайте пустой **публичный** репозиторий на GitHub с этим именем.
3. Установите [GitHub CLI](https://cli.github.com/) и выполните `gh auth login`.
4. В папке `launcher/`:

```bash
npm run publish:github -- --bump
```

5. Закоммитьте обновлённый `modpack-manifest.json` из этой папки и `git push`.

Игроки жмут **«Обновить»** в лаунчере — качаются только изменённые файлы.
