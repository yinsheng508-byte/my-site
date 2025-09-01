# 超简静态网站模板（适合 GitHub Pages / Netlify）

> 中文新手友好，一次部署，马上上线。

## 包含什么？
- `index.html` 主页
- `styles.css` 样式
- `script.js` 少量交互
- `404.html` 404 页面（GitHub Pages 会自动使用）
- `robots.txt`、`sitemap.xml`（SEO 基础）
- `assets/favicon.svg` 网站图标
- `.nojekyll` 避免 Jekyll 处理（保险）

## 一键部署到 GitHub Pages（网页端，无需命令行）
1. 注册并登录 GitHub：https://github.com
2. 右上角 ➜ **+** ➜ **New repository**  
   - Repository name 随意（如 `my-site`）
   - 公开 Public
   - **Create repository**
3. 点击 **Add file** ➜ **Upload files**，把本项目所有文件拖进去 ➜ **Commit changes**
4. 进入仓库 **Settings** ➜ **Pages**  
   - Build and deployment ➜ **Source: Deploy from a branch**  
   - Branch 选择 **main**，文件夹选择 **/**（root），**Save**
5. 等 0.5–2 分钟，回到 **Pages** 页面，会看到网站地址，形如：  
   `https://<你的用户名>.github.io/my-site/`

> 若想使用主站（不带仓库名），可把仓库命名为 `<你的用户名>.github.io`。

## 绑定自定义域名（可选）
- 推荐把 `www` 子域名 CNAME 到：`<你的用户名>.github.io`
- 在 GitHub 仓库 **Settings → Pages → Custom domain** 填写 `www.你的域名.com` 并保存  
- 稍等片刻，**Enforce HTTPS** 按钮可用时勾选，自动签发证书

> 顶级域名（不带 www）可在域名商设置 ALIAS/ANAME 到同一地址，或按域名商文档设置 A 记录到 GitHub Pages 官方 IP。

## 部署到 Netlify（拖拽版）
1. 访问 https://app.netlify.com/drop
2. 把本项目文件夹整体拖进去即可，完成后会得到一个 `*.netlify.app` 地址  
3. 在 Site settings 可绑定自定义域名并启用 HTTPS（自动）

## 表单（联系我）
- 本示例使用 Formspree。去 https://formspree.io/ 创建表单后，把 `index.html` 中 `<form>` 的 `action` 改成你的 endpoint

## 更新内容
- 直接在 GitHub 网页端点击文件编辑并 **Commit**，几秒内自动生效
