---
title: Markdown 扩展功能
published: 2024-05-01
updated: 2024-11-29
description: '阅读更多关于 Mizuki 中的 Markdown 功能'
image: ''
tags: [Demo, Example, Markdown, mizuki]
category: 'Examples'
draft: false 

---

## GitHub 仓库卡片

您可以添加链接到 GitHub 仓库的动态卡片，页面加载时，仓库信息会从 GitHub API 拉取。

::github{repo="matsuzaka-yuki/Mizuki"}

使用代码 `::github{repo="matsuzaka-yuki/Mizuki"}` 创建一个 GitHub 仓库卡片。

```markdown
::github{repo="matsuzaka-yuki/Mizuki"}
```

## 警示框

支持以下类型的警示框：`note` `tip` `important` `warning` `caution`

:::note
突出显示用户即使在浏览时也应考虑的信息。
:::

:::tip
帮助用户更成功的可选信息。
:::

:::important
用户成功所必需的关键信息。
:::

:::warning
因潜在风险而需要用户立即关注的关键内容。
:::

:::caution
行动的负面潜在后果。
:::

### 基本语法

```markdown
:::note
突出显示用户即使在浏览时也应考虑的信息。
:::

:::tip
帮助用户更成功的可选信息。
:::
```

### 自定义标题

警示框的标题可以自定义。

:::note[我的自定义标题]
这是一个带有自定义标题的备注。
:::

```markdown
:::note[我的自定义标题]
这是一个带有自定义标题的备注。
:::
```

### GitHub 语法

> [!TIP]
> [GitHub 语法](https://github.com/orgs/community/discussions/16925) 同样受支持。

```
> [!NOTE]
> GitHub 语法同样受支持。

> [!TIP]
> GitHub 语法同样受支持。
```

### 隐藏文本

您可以在文本中添加隐藏内容。该文本也支持 **Markdown** 语法。

这个内容 :spoiler[是隐藏的 **哎呀**]！

```markdown
这个内容 :spoiler[是隐藏的 **哎呀**]！
```