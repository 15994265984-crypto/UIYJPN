# 发布到公网

页面是纯静态网页，可以部署到 Vercel、Cloudflare Pages、Netlify 等静态托管服务。部署后会获得一个公网 HTTPS 地址；绑定自有域名还需要能修改该域名 DNS 的账户。

## GitHub Pages（免费 `github.io` 地址）

仓库根目录包含 `index.html` 和 `.github/workflows/pages.yml`。将文件推送到仓库的 `main` 分支后，工作流会自动发布站点。首次发布前，在 GitHub 仓库的 **Settings → Pages** 中将构建来源设为 **GitHub Actions**。

普通项目仓库的网址格式为 `https://<用户名>.github.io/<仓库名>/`。本仓库地址为 `https://15994265984-crypto.github.io/UIYJPN/`。GitHub Pages 提供这个 `github.io` 站点地址；注册独立域名（如 `.com`）需要通过域名注册商办理。

## Vercel

1. 将 `index.html` 上传到一个 GitHub 仓库，仓库根目录直接包含该文件。
2. 在 Vercel 导入该仓库，Framework Preset 选择 **Other**，Build Command 留空，Output Directory 填 `.`。
3. 部署完成后，可在项目设置的 Domains 中添加自有域名，并按 Vercel 显示的 DNS 记录在域名服务商处配置。

## 使用范围

站点托管后，任何浏览器都可以打开网页。网页读取的企业 PDF 仍由每位访问者在自己的浏览器中选择；文件在浏览器本地处理，不会随静态网页部署到托管服务。
