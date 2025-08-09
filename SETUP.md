# GitHub Repository Setup

## What's already created

✅ **Issues Templates** - forms for bug reports and feature requests  
✅ **Security Policy** - security policy  
✅ **Contributing Guidelines** - rules for contributors  
✅ **Documentation** - basic documentation  
✅ **OpenAPI Schema** - API specification  

## What needs to be configured manually

### 1. Enable Discussions

1. Go to **Settings** → **General**
2. Scroll to **Features** section
3. Enable **Discussions**
4. Create categories:
   - **Q&A** - questions about using the API
   - **General** - general discussions
   - **Announcements** - announcements and news

### 2. Create Labels

In **Issues** → **Labels** create:

- `bug` - bugs (red)
- `enhancement` - improvements (green)
- `breaking` - breaking changes (orange)
- `question` - questions (blue)
- `documentation` - documentation (light blue)
- `help wanted` - help needed (purple)

### 3. Enable GitHub Pages

1. **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: main
4. **Folder**: /docs
5. Save

The site will be available at: `https://it-incubator.github.io/musicfun-api/`

### 4. Create first release

1. Create tag: `v1.0.0`
2. **Releases** → **Create a new release**
3. Select tag
4. Fill in release notes:

```markdown
## 🚀 Initial Release

### ✨ Features
- REST API for working with music playlists
- Track, artist, and tag management
- Authorization via Bearer Token and API Key
- Pagination and filtering
- Image uploads

### 📚 Documentation
- OpenAPI 3.0 specification
- Interactive documentation (Swagger UI)
- Request examples
- GitHub Pages site

### 🔧 Technical
- JSON:API response format
- Standard HTTP status codes
- UTF-8 encoding
- CORS support
```

### 5. Pin important Issues/Discussions

Create and pin:

- **Roadmap** - API development plan
- **FAQ** - frequently asked questions
- **Migration Guide** - migration guide (when breaking changes appear)

## Repository structure

```
musicfun-api/
├── README.md                 # Main page
├── SECURITY.md              # Security policy
├── CONTRIBUTING.md          # Contribution rules
├── SETUP.md                 # This file
├── openapi/
│   └── openapi.yaml         # OpenAPI specification
├── docs/                    # GitHub Pages
│   ├── index.md             # Documentation main page
│   └── api.html             # Swagger UI
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug.yml          # Bug report form
        ├── feature.yml      # Feature request form
        └── config.yml       # Issues configuration
```

## Useful links

- **Documentation**: https://it-incubator.github.io/musicfun-api/
- **API Reference**: https://it-incubator.github.io/musicfun-api/api.html
- **Issues**: https://github.com/it-incubator/musicfun-api/issues
- **Discussions**: https://github.com/it-incubator/musicfun-api/discussions
- **Releases**: https://github.com/it-incubator/musicfun-api/releases

## Automation (optional)

For further automation you can add GitHub Actions:

- Automatic OpenAPI schema updates
- OpenAPI validation
- Automatic releases
- Slack/Discord notifications

Create file `.github/workflows/update-openapi.yml` if needed. 