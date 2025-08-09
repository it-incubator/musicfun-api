# Release Notes Template

## 🚨 Breaking changes
- Changes that break backward compatibility
- Example: `Removed deprecated endpoint /v1/old-endpoint`

## ✨ Features
- New features and capabilities
- Example: `Added endpoint /playlists/{id}/stats for getting statistics`

## 🐞 Fixes
- Bug fixes
- Example: `Fixed 500 error when getting playlist with empty title`

## 📚 Documentation
- Documentation updates
- Example: `Added examples for all endpoints in documentation`

## 🔧 Technical
- Technical changes
- Example: `Updated OpenAPI version to 3.1.0`

## 🚀 Performance
- Performance improvements
- Example: `Optimized database queries for getting playlists`

## 🔒 Security
- Security changes
- Example: `Added JWT token validation`

---

## Example filled release

## 🚀 v1.2.0

### ✨ Features
- Added endpoint `/playlists/{id}/stats` for getting playlist statistics
- Support for bulk operations for tracks
- Added filtering by creation date

### 🐞 Fixes
- Fixed 500 error when getting playlist with empty title
- Fixed pagination for large track lists
- Fixed email validation in user profile

### 📚 Documentation
- Added examples for all endpoints in documentation
- Updated authorization section
- Added FAQ to Discussions

### 🔧 Technical
- Updated OpenAPI version to 3.1.0
- Improved error handling
- Added request logging

### 🚀 Performance
- Optimized database queries for getting playlists
- Added caching for static data

---

## Migration (if there are breaking changes)

### Changes in v1.2.0

#### Breaking Changes
- Removed deprecated endpoint `/v1/old-endpoint`
- Changed response format for `/playlists` - added `stats` field

#### Migration Guide
1. Replace calls to `/v1/old-endpoint` with `/v2/new-endpoint`
2. Update `/playlists` response handling to support new `stats` field

#### Deprecation Timeline
- `v1.2.0`: `/v1/old-endpoint` marked as deprecated
- `v1.3.0`: `/v1/old-endpoint` will be removed 