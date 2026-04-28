---
layout: post
title: "用 GitHub Pages 搭建个人博客：从零开始"
date: 2024-01-15 09:00:00 +0800
categories: [技术]
tags: [Jekyll, GitHub Pages, 教程]
---

GitHub Pages 是一个免费的静态网站托管服务，结合 Jekyll 静态网站生成器，可以轻松搭建一个功能完整的个人博客。

本文记录了我搭建本站的完整过程，希望对有同样想法的朋友有所帮助。

## 前置准备

- 一个 GitHub 账号
- 基本的命令行使用经验
- （可选）了解 HTML / CSS 基础

## 第一步：创建仓库

在 GitHub 上创建一个名为 `{username}.github.io` 的仓库，其中 `{username}` 是你的 GitHub 用户名。这种命名格式会触发 GitHub Pages 的自动部署，访问 `https://{username}.github.io` 即可看到你的网站。

## 第二步：了解 Jekyll 目录结构

```
.
├── _config.yml       # 全局配置
├── _layouts/         # 页面模板
│   ├── default.html
│   ├── post.html
│   └── home.html
├── _includes/        # 可复用组件
│   ├── header.html
│   └── footer.html
├── _posts/           # 博客文章（Markdown）
│   └── 2024-01-01-my-first-post.md
├── assets/
│   └── css/
│       └── main.css
└── index.html
```

## 第三步：编写文章

所有文章放在 `_posts/` 目录下，文件名格式为 `YYYY-MM-DD-title.md`。

每篇文章的开头需要写 **Front Matter**（YAML 格式的元数据）：

```yaml
---
layout: post
title: "文章标题"
date: 2024-01-15 09:00:00 +0800
categories: [技术]
tags: [Jekyll, 教程]
---

这里是正文内容，支持 Markdown 语法。
```

## 第四步：本地预览

安装 Jekyll 后可以在本地实时预览效果：

```bash
bundle exec jekyll serve
```

浏览器访问 `http://localhost:4000` 即可看到网站。

## 第五步：推送并自动部署

```bash
git add .
git commit -m "Add new post"
git push origin main
```

推送后，GitHub Actions 会自动构建并部署。通常在 1~2 分钟内即可通过公网访问到最新内容。

## 小结

GitHub Pages + Jekyll 的组合具有以下优点：

| 优点 | 说明 |
|------|------|
| 免费 | 对个人用户完全免费 |
| 自动部署 | push 即部署，无需手动操作 |
| 版本控制 | 文章历史完整保存在 Git 中 |
| Markdown | 专注写作，无需关心排版 |
| 可定制 | 完全掌控样式和功能 |

如果你也想拥有一个自己的博客，不妨从今天开始！
