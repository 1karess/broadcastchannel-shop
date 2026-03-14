# 部署购物站到 GitHub Pages（不同 origin）

老师要求验证**不同 origin** 下的跨站追踪。当前：
- 新闻站：`site-alpha-alpha.vercel.app`（Vercel，origin: `*.vercel.app`）
- 购物站：`*.github.io`（GitHub Pages，origin: `*.github.io`）

两者为不同顶层域名，满足验证要求。

## 步骤

### 1. 在 GitHub 新建仓库

- 登录 GitHub → New repository
- 仓库名：`broadcastchannel-shop`
- 选择 Public，不勾选 README
- 创建

### 2. 推送代码

在终端执行（将 `YOUR_USERNAME` 换成你的 GitHub 用户名）：

```bash
cd /Users/karess/Desktop/instagram_decompiled/experiments/broadcastchannel_test/site-beta-github-pages

git init
git add index.html
git commit -m "Shopping site for BC experiment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/broadcastchannel-shop.git
git push -u origin main
```

### 3. 开启 GitHub Pages

- 仓库 → Settings → Pages
- Source: Deploy from a branch
- Branch: main，文件夹选 `/ (root)`
- Save

### 4. 等待部署

约 1–2 分钟后访问：`https://YOUR_USERNAME.github.io/broadcastchannel-shop/`

## 测试链接汇总

| 站点 | URL | Origin |
|------|-----|--------|
| 新闻站 | https://site-alpha-alpha.vercel.app | vercel.app |
| 购物站 | https://YOUR_USERNAME.github.io/broadcastchannel-shop/ | github.io |
| Dashboard | https://broadcastchanneltest.vercel.app/dashboard | - |

在 Facebook WebView 中先打开新闻站，再打开购物站，然后在电脑上查看 Dashboard 是否出现跨站关联数据。
