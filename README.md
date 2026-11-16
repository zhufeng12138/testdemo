# testdemo

一个最简单的静态网页工作流：纯 HTML 页面 + GitHub Actions 自动部署到 GitHub Pages。

## 本地预览

直接在浏览器中打开 `index.html`，或在仓库目录运行：

```bash
python -m http.server 8000
```

然后访问 <http://localhost:8000>。

## 自动部署

1. 在 GitHub 仓库 **Settings → Pages → Build and deployment** 中，将 **Source** 设为 **GitHub Actions**。
2. 把改动推送到 `main` 分支。
3. `.github/workflows/deploy-pages.yml` 会自动运行，将仓库根目录内容部署到 GitHub Pages。

也可以在仓库 **Actions** 页面手动触发 **Deploy static site to GitHub Pages**。

部署完成后，页面地址会显示为 `https://<用户名>.github.io/<仓库名>/`。
