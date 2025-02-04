![](docs/public/combine.webp)

# AI as Workspace

精心设计的 AI 客户端

[网站链接](https://aiaw.app) - [使用文档](https://docs.aiaw.app/) - [自部署指南](https://docs.aiaw.app/self-host/)

## 功能概览

### 对话页面

- 用户输入预览
- 修改提问、重新生成 以分叉的形式呈现
- 自定义键盘快捷键
- 对齐到消息开头/结尾的快速滚动

<img src="https://fs.krytro.com/aiaw/dialog.webp" width="600">

### 细节设计

- 支持将文本类型文件（代码、csv等）作为附件，AI 能看到文件内容和文件名；避免文件内容占据显示空间
- 对于大段的文本，可在**输入框外**使用 Ctrl + V 粘贴，也将作为附件；避免大段内容占据显示空间

<img src="https://fs.krytro.com/aiaw/text-item.webp" width="600">

- 可在用户输入中引用先前消息中的内容，方便对助手回答的部分内容针对性地追问
- 选中多行消息文本后，可直接复制 Markdown 原文

<img src="https://fs.krytro.com/aiaw/text-selection.webp" width="600">

- 粘贴从 VSCode 复制的代码时，自动用代码块包裹，并标明语言

<img src="https://fs.krytro.com/aiaw/paste-code.webp" width="600">

### 多工作区

- 创建多个工作区，将不同主题的对话分隔开
- 可将多个工作区放入一个文件夹中；支持嵌套
- 一个工作区中可创建多个助手，也可以创建全局助手

<img src="docs/usage/res/workspace-list.png" width="378">

### 数据储存

- 数据首先储存在本地，无需加载且离线可浏览
- 登录后可使用云同步，跨设备实时同步
- 多窗口协同支持：同一浏览器打开多个标签，数据响应式同步

### [Artifacts](https://docs.aiaw.app/usage/artifacts.html)

- 可将助手回答的任意部分转为 Artifacts
- 用户可编辑，带版本控制，代码高亮
- 可控制助手对 Artifacts 的读写权限
- 可同时打开多个 Artifacts

<img src="https://fs.krytro.com/aiaw/convert-artifact.webp" width="600">

### [插件系统](https://docs.aiaw.app/usage/plugins.html)

- 内置计算器、[文档解析、视频解析](https://docs.aiaw.app/usage/file-parse.html)、图像生成等插件
- 可在插件市场安装更多插件
- 可将 Gradio 应用配置为插件；兼容部分 LobeChat 插件；
- 插件不只是工具调用

![](docs/public/plugin-market.png)

### 轻量，高性能

- 启动迅速，无需等待
- 切换对话丝滑流畅

<img src="https://fs.krytro.com/aiaw/switch-dialog.webp" width="600">

### [动态提示词](https://docs.aiaw.app/usage/prompt-vars.html)

- 通过创建提示词变量，使用模板语法，构建动态可复用的提示词
- 抽离提示词中的重复部分，放入工作区变量，实现提示词的复用

<img src="docs/usage/res/assistant-prompt-vars.png" width="378">

### 其他功能

多服务商支持、助手市场、深色模式、自定义主题色、[跨平台](https://docs.aiaw.app/usage/cross-platform.html)

[网站链接](https://aiaw.app) - [使用文档](https://docs.aiaw.app/) - [自部署指南](https://docs.aiaw.app/self-host/)

## LightHouse

| Desktop | Mobile |
| :-----: | :----: |
| ![](docs/public/lighthouse_score_desktop.png) | ![](docs/public/lighthouse_score_mobile.png) |

## 相关项目

- [New API](https://github.com/Calcium-Ion/new-api): AI模型接口管理与分发系统，支持将多种大模型转为OpenAI格式调用

## Roadmap

- [ ] 补全文档

- [x] Docker 自部署

- [ ] i18n

## Install the dependencies
```bash
pnpm i
```

### Start the app in development mode (hot-code reloading, error reporting, etc.)
```bash
quasar dev
```

### Lint the files
```bash
pnpm lint
```

### Build the app for production
```bash
# SPA
quasar build

# PWA
quasar build -m pwa
```
