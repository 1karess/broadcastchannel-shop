# BroadcastChannel 实验 - 购物站 (GitHub Pages)

用于验证跨 **不同 origin** 的 BroadcastChannel 追踪。

- **新闻站**：`site-alpha-alpha.vercel.app`（Vercel，origin: vercel.app）
- **购物站**：https://1karess.github.io/broadcastchannel-shop/（GitHub Pages，origin: github.io）

两个顶层站点来自不同域名，均嵌入同一第三方 tracker iframe。

## 部署到 GitHub Pages

1. 在 GitHub 新建仓库，名称例如 `broadcastchannel-shop`
2. 将本文件夹内的 `index.html` 推送到仓库根目录
3. 仓库 Settings → Pages → Source 选择 `main` 分支，根目录 `/`
4. 等待部署完成，访问 https://1karess.github.io/broadcastchannel-shop/

## 测试链接

- 新闻站：https://site-alpha-alpha.vercel.app
- 购物站：https://1karess.github.io/broadcastchannel-shop/
- Dashboard：https://bc-tracker-karess.pages.dev/dashboard
