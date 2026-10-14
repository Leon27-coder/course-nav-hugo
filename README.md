# 课程资料导航页

一个基于 [Hugo](https://gohugo.io/) + [WebStack-Hugo](https://github.com/shenweiyan/WebStack-Hugo) 主题搭建的课程资料导航站：**分类展示、标题搜索、点击直达**。

## 功能特性

- **分类展示**：左侧边栏按主题分组（AI 与大模型 / 编程开发 / 职场技能 / 学习平台），快速定位所需资料
- **标题搜索**：顶部搜索框按标题关键词实时过滤
- **点击直达**：点击卡片在新标签页打开资料链接
- **响应式布局**：桌面 / 平板 / 手机自适应

## 本地运行

```bash
# 依赖：Hugo extended v0.167+（https://gohugo.io/installation/）
hugo server
```

浏览器打开 <http://localhost:1313/> 即可预览，改动文件后自动热更新。

## 如何维护资料

所有导航条目集中在 `data/webstack.yml` 一个文件中，按四级结构组织：

```yaml
- taxonomy: 分类名称            # 一级分类（侧边栏分组）
  icon: fas fa-book             # 分类图标（FontAwesome 类名）
  list:
    - term: 子分类名称          # 二级分类
      links:
        - title: 资料标题
          url: https://example.com
          description: 一句话介绍
```

新增分类或资料只需仿照现有格式追加即可，无需改动任何代码。

## 自动部署

推送到 `main` 分支后，GitHub Actions 会自动构建站点并发布到 GitHub Pages（工作流见 `.github/workflows/hugo.yml`）。

首次使用需在仓库 **Settings → Pages → Build and deployment → Source** 中选择 **GitHub Actions**。

## 致谢

- 主题：[WebStack-Hugo](https://github.com/shenweiyan/WebStack-Hugo)（MIT License）
- 原始设计：[WebStackPage/WebStackPage.github.io](https://github.com/WebStackPage/WebStackPage.github.io)

## License

[MIT](./LICENSE)
