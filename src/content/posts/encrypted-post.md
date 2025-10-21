---
title: 加密文章
published: 2024-01-15
description: 这是一篇用于测试页面加密功能的文章
encrypted: true
pinned: true
password: "123456"
tags: ["测试", "加密"]
category: "技术"

---

此博客模板使用 [Astro](https://astro.build/) 构建。对于本指南中未提及的事项，您可以在 [Astro 文档](https://docs.astro.build/) 中找到答案。

## 文章的前言配置

```yaml
---
title: My First Blog Post
published: 2023-09-09
description: This is the first post of my new Astro blog.
image: ./cover.jpg
tags: [Foo, Bar]
category: Front-end
draft: false
---
```

| 属性          | 描述                                                         |
| ------------- | ------------------------------------------------------------ |
| `title`       | 文章的标题。                                                 |
| `published`   | 文章的发布日期。                                             |
| `pinned`      | 是否将此文章置顶于文章列表顶部。                             |
| `description` | 文章的简短描述。显示在索引页上。                             |
| `image`       | 文章的封面图片路径。<br/>1. 以 `http://` 或 `https://` 开头：使用网络图片<br/>2. 以 `/` 开头：指向 `public` 目录中的图片<br/>3. 无上述前缀：相对于 markdown 文件的位置 |
| `tags`        | 文章的标签。                                                 |
| `category`    | 文章的分类。                                                 |
| `licenseName` | 文章内容的许可证名称。                                       |
| `author`      | 文章的作者。                                                 |
| `sourceLink`  | 文章内容的来源链接或参考。                                   |
| `draft`       | 如果文章仍是草稿，则不会显示。                               |

## 文章文件的存放位置

您的文章文件应放置在 `src/content/posts/` 目录下。您也可以创建子目录来更好地组织您的文章和资源。

```
src/content/posts/
├── post-1.md
└── post-2/
    ├── cover.png
    └── index.md
```