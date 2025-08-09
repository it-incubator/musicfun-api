# MusicFun API Documentation

- 📦 **OpenAPI**: `/openapi/openapi.yaml`
- 🧭 **Live API Reference**: [API Reference](./api.html)
- 🗂️ **Q&A**: [Discussions → Q&A](https://github.com/it-incubator/musicfun-api/discussions/categories/q-a)
- 🚀 **Roadmap**: see pinned issue / [Discussions → Announcements](https://github.com/it-incubator/musicfun-api/discussions/categories/announcements)
- 📝 **Latest release**: [Releases](https://github.com/it-incubator/musicfun-api/releases)

## Quick Start

### Basic Information
- **Base URL**: `https://musicfun.it-incubator.app`
- **Authorization**: Bearer Token or API Key
- **Data Format**: JSON
- **Encoding**: UTF-8

### Authorization

The API supports two types of authorization:

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

### Request Examples

#### Get Playlists
```bash
curl -H "Authorization: Bearer $TOKEN" \
     "https://musicfun.it-incubator.app/playlists?pageNumber=1&pageSize=10"
```

#### Create Playlist
```bash
curl -X POST \
     -H "Authorization: Bearer $TOKEN" \
     -H "Content-Type: application/json" \
     -d '{
       "name": "My Playlist",
       "description": "Playlist description"
     }' \
     https://musicfun.it-incubator.app/playlists
```

#### Get Track
```bash
curl -H "Authorization: Bearer $TOKEN" \
     https://musicfun.it-incubator.app/tracks/TRACK_ID
```

## Main Endpoints

### Playlists
- `GET /playlists` - Get list of playlists
- `POST /playlists` - Create playlist
- `GET /playlists/{id}` - Get playlist by ID
- `PUT /playlists/{id}` - Update playlist
- `DELETE /playlists/{id}` - Delete playlist

### Tracks
- `GET /tracks` - Get list of tracks
- `POST /tracks` - Create track
- `GET /tracks/{id}` - Get track by ID
- `PUT /tracks/{id}` - Update track
- `DELETE /tracks/{id}` - Delete track

### Artists
- `GET /artists` - Get list of artists
- `POST /artists` - Create artist
- `GET /artists/{id}` - Get artist by ID

### Tags
- `GET /tags` - Get list of tags
- `POST /tags` - Create tag
- `GET /tags/{id}` - Get tag by ID

## Pagination

The API uses pagination for large lists:

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

## Error Handling

The API returns standard HTTP status codes:

- `200` - Successful request
- `201` - Resource created
- `204` - Successful request without response body
- `400` - Bad request
- `401` - Unauthorized
- `403` - Forbidden
- `404` - Resource not found
- `500` - Internal server error

## Support

- **Questions**: [Discussions (Q&A)](https://github.com/it-incubator/musicfun-api/discussions/categories/q-a)
- **Bug Reports**: [Issues](https://github.com/it-incubator/musicfun-api/issues)
- **Vulnerabilities**: [Security Policy](https://github.com/it-incubator/musicfun-api/blob/main/SECURITY.md) 