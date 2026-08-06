# my-blog-prov (部署发布专用仓库)

这是开源项目 [YuanYii/my-blog](https://github.com/YuanYii/my-blog) 的**自动化部署物料与发布仓库**。

## 💡 为什么需要这个仓库？
为了保证主源码仓库的纯净，本项目将“源码”与“部署物料”解耦。
本仓库仅用于存放由自动化脚本构建出的 **GitHub Release 资源**，不包含业务源码，作为一个完全公开的部署资源分发地。

## 📦 里面有什么？
每个 Release 版本中包含：
- `deploy-bundle-vX.Y.Z.zip`（冷部署合包，推荐）
- `blog-app.jar`（Spring Boot 可执行后端）
- `frontend-static.tar.gz`（Nuxt 静态前端页面）
- `deploy-server.sh`（一键部署脚本）
- 及配套的数据库迁移与备份脚本

## 🚀 部署方式
在您的全新服务器上只需执行：
```bash
curl -L https://github.com/YuanYii/my-blog-prov/releases/latest/download/deploy-server.sh -o deploy-server.sh
chmod +x deploy-server.sh
GITHUB_REPO=YuanYii/my-blog-prov sudo -E ./deploy-server.sh
```

> 💡 浏览器打开 `http://<服务器IP>/` 即可访问首页。
> 默认后台入口：`/admin/login`，默认账号/密码：`admin / 123456`。
> 更多详情和部署参数请查阅源码项目文档：[YuanYii/my-blog](https://github.com/YuanYii/my-blog)
