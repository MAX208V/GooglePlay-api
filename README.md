# Google Play API

> 本项目基于 [facundoolano/google-play-api](https://github.com/facundoolano/google-play-api) 部署，将 [google-play-scraper](https://github.com/facundoolano/google-play-scraper/) 封装为 RESTful API。

## 本地运行

```bash
npm install
npm start
```

## 示例请求

所有接口参数均来自 google-play-scraper，完整参数请参考其[官方文档](https://github.com/facundoolano/google-play-scraper/#usage)。

### 获取免费应用排行榜（默认列表）

```http
GET /api/apps/
```

### 获取免费应用排行榜（含完整详情）

```http
GET /api/apps/?fullDetail=true
```

### 获取俄罗斯地区畅销动作游戏

```http
GET /api/apps/?collection=topselling_paid&category=GAME_ACTION&country=ru
```

### 获取应用详情

```http
GET /api/apps/org.wikipedia/
```

### 获取应用详情（西班牙语）

```http
GET /api/apps/org.wikipedia/?lang=es
```

### 获取应用权限信息（含完整描述）

```http
GET /api/apps/org.wikipedia/permissions/
```

### 获取应用权限信息（简略列表）

```http
GET /api/apps/org.wikipedia/permissions/?short=true
```

### 获取应用数据安全信息

```http
GET /api/apps/org.wikipedia/datasafety/
```

### 获取相似应用

```http
GET /api/apps/org.wikipedia/similar/
```

### 获取应用评论

```http
GET /api/apps/org.wikipedia/reviews/
```

### 搜索应用

```http
GET /api/apps/?q=facebook
```

### 获取搜索建议

```http
GET /api/apps/?suggest=face
```

### 获取开发者发布的所有应用

```http
GET /api/developers/Wikimedia%20Foundation/
```

### 获取所有分类

```http
GET /api/categories/
```

---

## 手动同步源仓库

本项目使用 GitHub Actions 手动触发同步：

1. 进入仓库的 **Actions** 页面
2. 选择 **Sync from Upstream** 工作流
3. 点击 **Run workflow** 按钮
4. 确认执行即可同步最新代码

---

## 来源声明

- **原项目**: [facundoolano/google-play-api](https://github.com/facundoolano/google-play-api)
- **作者**: Facundo Olano
- **许可证**: MIT License
