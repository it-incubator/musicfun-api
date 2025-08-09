# MusicFun API Documentation

- 📦 **OpenAPI**: `/openapi/openapi.yaml`
- 🧭 **Live API Reference**: [API Reference](./api.html)
- 🗂️ **Q&A**: [Discussions → Q&A](https://github.com/it-incubator/musicfun-api/discussions/categories/q-a)
- 🚀 **Roadmap**: см. pinned issue / [Discussions → Announcements](https://github.com/it-incubator/musicfun-api/discussions/categories/announcements)
- 📝 **Latest release**: [Releases](https://github.com/it-incubator/musicfun-api/releases)

## Быстрый старт

### Базовая информация
- **Base URL**: `https://musicfun.it-incubator.app`
- **Авторизация**: Bearer Token или API Key
- **Формат данных**: JSON
- **Кодировка**: UTF-8

### Авторизация

API поддерживает два типа авторизации:

#### Bearer Token
```bash
curl -H "Authorization: Bearer YOUR_TOKEN" \
     https://musicfun.it-incubator.app/playlists
```

#### API Key
```bash
curl -H "X-API-Key: YOUR_API_KEY" \
     https://musicfun.it-incubator.app/playlists
```

### Примеры запросов

#### Получение плейлистов
```bash
curl -H "Authorization: Bearer $TOKEN" \
     "https://musicfun.it-incubator.app/playlists?pageNumber=1&pageSize=10"
```

#### Создание плейлиста
```bash
curl -X POST \
     -H "Authorization: Bearer $TOKEN" \
     -H "Content-Type: application/json" \
     -d '{
       "name": "Мой плейлист",
       "description": "Описание плейлиста"
     }' \
     https://musicfun.it-incubator.app/playlists
```

#### Получение трека
```bash
curl -H "Authorization: Bearer $TOKEN" \
     https://musicfun.it-incubator.app/tracks/TRACK_ID
```

## Основные эндпоинты

### Плейлисты
- `GET /playlists` - Получить список плейлистов
- `POST /playlists` - Создать плейлист
- `GET /playlists/{id}` - Получить плейлист по ID
- `PUT /playlists/{id}` - Обновить плейлист
- `DELETE /playlists/{id}` - Удалить плейлист

### Треки
- `GET /tracks` - Получить список треков
- `POST /tracks` - Создать трек
- `GET /tracks/{id}` - Получить трек по ID
- `PUT /tracks/{id}` - Обновить трек
- `DELETE /tracks/{id}` - Удалить трек

### Артисты
- `GET /artists` - Получить список артистов
- `POST /artists` - Создать артиста
- `GET /artists/{id}` - Получить артиста по ID

### Теги
- `GET /tags` - Получить список тегов
- `POST /tags` - Создать тег
- `GET /tags/{id}` - Получить тег по ID

## Пагинация

API использует пагинацию для больших списков:

```json
{
  "data": [...],
  "meta": {
    "totalCount": 100,
    "page": 1,
    "pageSize": 20,
    "pagesCount": 5
  }
}
```

## Обработка ошибок

API возвращает стандартные HTTP коды состояния:

- `200` - Успешный запрос
- `201` - Ресурс создан
- `204` - Успешный запрос без тела ответа
- `400` - Неверный запрос
- `401` - Не авторизован
- `403` - Доступ запрещен
- `404` - Ресурс не найден
- `500` - Внутренняя ошибка сервера

## Поддержка

- **Вопросы**: [Discussions (Q&A)](https://github.com/it-incubator/musicfun-api/discussions/categories/q-a)
- **Баг-репорты**: [Issues](https://github.com/it-incubator/musicfun-api/issues)
- **Уязвимости**: [Security Policy](https://github.com/it-incubator/musicfun-api/blob/main/SECURITY.md) 