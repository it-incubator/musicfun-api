# MusicFun API

[Docs](https://it-incubator.github.io/musicfun-api/) ·
[API Reference](https://it-incubator.github.io/musicfun-api/api.html) ·
[Releases](https://github.com/it-incubator/musicfun-api/releases) ·
[Q&A](https://github.com/it-incubator/musicfun-api/discussions/categories/q-a)

## О проекте

MusicFun API предоставляет REST API для работы с музыкальными плейлистами, треками, артистами и тегами.

## Быстрый старт

- **База URL**: `https://musicfun.it-incubator.app`
- **Авторизация**: Bearer Token или API Key
- **Документация**: [Swagger UI](https://musicfun.it-incubator.app/api)

### Пример запроса

```bash
curl -H "Authorization: Bearer $TOKEN" \
     https://musicfun.it-incubator.app/playlists
```

## Сообщить о проблеме

Откройте issue через форму (Bug report / Feature request). Для вопросов — Discussions (Q&A).

## Версионирование

SemVer. Breaking changes помечаются в релиз-нотах.

## Поддерживаемые версии

Мы поддерживаем только последние две минорные версии API. 