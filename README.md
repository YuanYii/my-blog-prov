# my-blog-prov

my-blog 部署专用仓库。

本仓只放 GitHub Release assets（jar / static / sql / 部署脚本），代码仓在 [YuanYii/my-blog](https://github.com/YuanYii/my-blog)。

## 部署方式

参见每个 release 的 assets：
- `deploy-bundle-vX.Y.Z.zip` 冷部署包（推荐，1 个文件拉完）
- `blog-app.jar` Spring Boot fat jar
- `frontend-static.tar.gz` Nuxt 生成的静态文件
- `schema-sqlite.sql` SQLite 初始化
- `deploy-server.sh` 服务器端一键部署脚本
- `SHA256SUMS` 校验文件

服务器端：
```bash
export GITHUB_REPO=YuanYii/my-blog-prov
sudo ./deploy-server.sh v2.7.0
```
