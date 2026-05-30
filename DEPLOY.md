# 部署说明

这个项目是纯静态网站，只需要托管根目录文件即可，不需要服务器。

## 推荐方案：GitHub + Cloudflare Pages

适合长期维护、自动部署和绑定域名。

### 1. 创建 GitHub 仓库

在 GitHub 新建一个仓库，例如：

```text
tea-prompt-generator
```

### 2. 上传文件

上传这些文件：

```text
index.html
prompt-generator.html
README.md
CHANGELOG.md
DEPLOY.md
```

### 3. 连接 Cloudflare Pages

1. 登录 Cloudflare
2. 进入 `Workers & Pages`
3. 选择 `Create application`
4. 选择 `Pages`
5. 连接 GitHub 仓库
6. 选择这个项目仓库

### 4. 构建设置

因为这是纯静态 HTML，不需要构建命令。

```text
Build command: 留空
Build output directory: /
Root directory: /
```

如果 Cloudflare 要求填写输出目录，可以填：

```text
.
```

### 5. 发布

点击部署后，会得到一个类似这样的地址：

```text
https://tea-prompt-generator.pages.dev
```

之后每次更新 GitHub 仓库，Cloudflare Pages 会自动重新部署。

## 备选方案：GitHub Pages

适合最简单的免费托管。

1. 把项目上传到 GitHub
2. 进入仓库 `Settings`
3. 找到 `Pages`
4. Source 选择 `Deploy from a branch`
5. Branch 选择 `main`
6. Folder 选择 `/root`
7. 保存

访问地址通常是：

```text
https://你的用户名.github.io/仓库名/
```

## 备选方案：Vercel

适合后续扩展成更复杂的前端项目。

1. 登录 Vercel
2. Import Git Repository
3. 选择 GitHub 仓库
4. Framework Preset 选择 `Other`
5. Build Command 留空
6. Output Directory 留空或填 `.`
7. Deploy

## 更新流程

后续维护建议按这个流程：

```text
修改 index.html
本地打开检查
提交到 GitHub
等待 Cloudflare Pages / Vercel 自动部署
打开线上地址确认
```
