# 海边之旅 · 地图行程

手机浏览器打开本站即可查看行程地图，并一键跳转高德导航。

## 高德 Key 域名白名单（必做）

在 [高德控制台](https://console.amap.com/dev/key/app) 给该 Web端 Key 增加：

- `*.github.io`
- 你的完整 Pages 域名，例如 `用户名.github.io`

本地调试可临时填 `*`。

## 发布到 GitHub Pages

若本机已安装 Git 与 GitHub CLI：

```powershell
cd "C:\Users\DT208\Documents\coast-trip-map"
gh auth login
gh repo create coast-trip-map --public --source=. --remote=origin --push
gh pages --help 2>
# 或在仓库 Settings → Pages → Branch: main / root
```

也可在网页新建空仓库后：

```powershell
cd "C:\Users\DT208\Documents\coast-trip-map"
git init
git add .
git commit --trailer "Co-authored-by: Cursor <cursoragent@cursor.com>" -m "Publish coastal trip map for GitHub Pages"
git branch -M main
git remote add origin https://github.com/你的用户名/coast-trip-map.git
git push -u origin main
```

然后打开仓库 Settings → Pages → Source: Deploy from branch → main → / (root) → Save。
