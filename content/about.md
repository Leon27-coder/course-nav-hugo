---
title: "关于网站"
date: 2026-10-13T19:00:00+08:00
draft: false
---

#### 这是一个「课程资料导航」演示站点

本站基于开源 Hugo 主题 [WebStack-Hugo](https://github.com/shenweiyan/WebStack-Hugo)（MIT License）搭建，用于集中管理和快速访问各类课程学习资料。

<br/>

#### 功能特性

- **分类展示**：按主题分为 AI 与大模型、编程开发、职场技能、学习平台四大类，左侧边栏可快速定位；
- **标题搜索**：顶部搜索框支持按标题关键词实时过滤；
- **点击直达**：点击卡片直接在新标签页打开资料链接。

<br/>

#### 数据如何维护

所有导航条目都保存在站点根目录的 `data/webstack.yml` 一个文件里，按 `taxonomy → list → term → links` 四级结构组织，新增分类或条目只需仿照现有格式追加几行即可，无需改动任何代码。

<br/>

#### 本地预览方式

```bash
hugo server -D
```

然后在浏览器打开 <http://localhost:1313/> 即可查看效果。
