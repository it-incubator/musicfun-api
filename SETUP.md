# Настройка GitHub репозитория

## Что уже создано

✅ **Issues Templates** - формы для баг-репортов и фич-реквестов  
✅ **Security Policy** - политика безопасности  
✅ **Contributing Guidelines** - правила для контрибьюторов  
✅ **Documentation** - базовая документация  
✅ **OpenAPI Schema** - спецификация API  

## Что нужно настроить вручную

### 1. Включить Discussions

1. Перейдите в **Settings** → **General**
2. Прокрутите до секции **Features**
3. Включите **Discussions**
4. Создайте категории:
   - **Q&A** - вопросы по использованию API
   - **General** - общие обсуждения
   - **Announcements** - анонсы и новости

### 2. Создать Labels

В **Issues** → **Labels** создайте:

- `bug` - баги (красный)
- `enhancement` - улучшения (зеленый)
- `breaking` - breaking changes (оранжевый)
- `question` - вопросы (синий)
- `documentation` - документация (голубой)
- `help wanted` - нужна помощь (фиолетовый)

### 3. Включить GitHub Pages

1. **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: main
4. **Folder**: /docs
5. Сохраните

Сайт будет доступен по адресу: `https://it-incubator.github.io/musicfun-api/`

### 4. Создать первый релиз

1. Создайте тег: `v1.0.0`
2. **Releases** → **Create a new release**
3. Выберите тег
4. Заполните релиз-ноты:

```markdown
## 🚀 Initial Release

### ✨ Features
- REST API для работы с музыкальными плейлистами
- Управление треками, артистами и тегами
- Авторизация через Bearer Token и API Key
- Пагинация и фильтрация
- Загрузка изображений

### 📚 Documentation
- OpenAPI 3.0 спецификация
- Интерактивная документация (Swagger UI)
- Примеры запросов
- GitHub Pages сайт

### 🔧 Technical
- JSON:API формат ответов
- Стандартные HTTP коды состояния
- UTF-8 кодировка
- CORS поддержка
```

### 5. Закрепить важные Issues/Discussions

Создайте и закрепите:

- **Roadmap** - план развития API
- **FAQ** - часто задаваемые вопросы
- **Migration Guide** - руководство по миграции (когда появятся breaking changes)

## Структура репозитория

```
musicfun-api/
├── README.md                 # Главная страница
├── SECURITY.md              # Политика безопасности
├── CONTRIBUTING.md          # Правила контрибьюции
├── SETUP.md                 # Этот файл
├── openapi/
│   └── openapi.yaml         # OpenAPI спецификация
├── docs/                    # GitHub Pages
│   ├── index.md             # Главная страница документации
│   └── api.html             # Swagger UI
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug.yml          # Форма баг-репорта
        ├── feature.yml      # Форма фич-реквеста
        └── config.yml       # Конфигурация issues
```

## Полезные ссылки

- **Документация**: https://it-incubator.github.io/musicfun-api/
- **API Reference**: https://it-incubator.github.io/musicfun-api/api.html
- **Issues**: https://github.com/it-incubator/musicfun-api/issues
- **Discussions**: https://github.com/it-incubator/musicfun-api/discussions
- **Releases**: https://github.com/it-incubator/musicfun-api/releases

## Автоматизация (опционально)

Для автоматизации можно добавить GitHub Actions:

- Автоматическое обновление OpenAPI схемы
- Проверка валидности OpenAPI
- Автоматические релизы
- Уведомления в Slack/Discord

Создайте файл `.github/workflows/update-openapi.yml` при необходимости. 