# 茶叶文生图提示词生成器

一个纯静态 HTML 工具导航站，内置茶叶主题文生图提示词生成器，并收纳常用 AI 对话和图像工具入口。提示词生成器支持商业 KV、产品摄影、礼盒包装、茶空间、知识图鉴、水墨意境、微缩景观、节气插画等方向。

## 功能

- 选择图片类型、茶叶品类、画幅和构图
- 独立控制核心画面、植物元素、场景元素、人物元素、茶具与信息元素
- 独立控制画面结构、风格质感、材质、光影、主色系、氛围、质量和负面词
- 自动生成完整提示词
- 一键复制生成结果
- 导航到 ChatGPT、Gemini、豆包、Claude、Kimi、DeepSeek、即梦 AI、Midjourney、LiblibAI 等外部工具
- 无需后端、数据库或构建工具

## 文件结构

```text
.
├── index.html
├── prompt-generator.html
├── README.md
├── CHANGELOG.md
└── DEPLOY.md
```

## 本地预览

直接双击 `index.html` 即可打开导航页。

提示词生成器页面位于：

```text
prompt-generator.html
```

也可以用本地静态服务器预览：

```bash
python3 -m http.server 8765
```

然后访问：

```text
http://127.0.0.1:8765/
```

## 推荐部署方式

长期维护建议使用：

- GitHub + Cloudflare Pages
- GitHub + Vercel
- GitHub Pages

详细步骤见 [DEPLOY.md](./DEPLOY.md)。

## 维护建议

- 新增导航入口：编辑 `index.html` 中的工具卡片
- 新增茶叶品类：编辑 `prompt-generator.html` 中的 `teaTypes`
- 新增图片类型：编辑 `prompt-generator.html` 中的 `visualTypes`
- 新增构图：编辑 `prompt-generator.html` 中的 `compositions`
- 新增风格：编辑 `prompt-generator.html` 中的 `styles`
- 新增画面结构：编辑 `prompt-generator.html` 中的 `spacePresets`
- 新增材质、光影、色彩、氛围：分别编辑对应的 preset 数组

每次修改后，建议至少测试：

- 页面能正常打开
- 下拉选项能正常切换
- 生成结果会跟随选项变化
- 复制按钮可用
