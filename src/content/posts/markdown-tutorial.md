---
title: Markdown 教程
published: 2025-01-20
pinned: true
description: 一个简单的 Markdown 博客文章示例。
tags: [Markdown, Blogging]
category: Examples
licenseName: "Unlicensed"
author: emn178
sourceLink: "https://github.com/emn178/markdown"
draft: false

---

# Markdown 教程

一个 Markdown 示例展示如何编写 markdown 文件。本文档整合了核心语法和扩展功能（GMF）。

- [块元素](#块元素)
  - [段落和换行](#段落和换行)
  - [标题](#标题)
  - [块引用](#块引用)
  - [列表](#列表)
  - [代码块](#代码块)
  - [水平分割线](#水平分割线)
  - [表格](#表格)
- [行内元素](#行内元素)
  - [链接](#链接)
  - [强调](#强调)
  - [代码](#代码)
  - [图片](#图片)
  - [删除线](#删除线)
- [其他功能](#其他功能)
  - [自动链接](#自动链接)
  - [反斜杠转义](#反斜杠转义)
- [行内 HTML](#行内-html)

## 块元素

### 段落和换行

#### 段落

HTML 标签: `<p>`

一个或多个空行。（空行是指只包含**空格**或**制表符**的行。）

代码:

    This will be
    inline.
    
    This is second paragraph.

预览:

---

This will be
inline.

This is second paragraph.

---

#### 换行

HTML 标签: `<br />`

以**两个或更多空格**结束一行。

代码:

    This will be not
    inline.

预览:

---

This will be not  
inline.

---

### 标题

Markdown 支持两种标题样式：Setext 和 atx。

#### Setext

HTML 标签: `<h1>`, `<h2>`

使用任意数量的**等号（=）**作为 `<h1>` 和**破折号（-）**作为 `<h2>` 来"下划线"。

代码:

    This is an H1
    =============
    This is an H2
    -------------

预览:

---

# This is an H1

## This is an H2

---

#### atx

HTML 标签: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

在行首使用 1-6 个**井号（#）**，对应 `<h1>` - `<h6>`。

代码:

    # This is an H1
    ## This is an H2
    ###### This is an H6

预览:

---

# This is an H1

## This is an H2

###### This is an H6

---

可选地，您可以"关闭"atx 样式的标题。关闭的井号**不需要匹配**打开标题使用的井号数量。

代码:

    # This is an H1 #
    ## This is an H2 ##
    ### This is an H3 ######

预览:

---

# This is an H1

## This is an H2

### This is an H3

---

### 块引用

HTML 标签: `<blockquote>`

Markdown 使用电子邮件样式的 **>** 字符进行块引用。如果您对文本进行硬换行并在每行前加上 >，效果最佳。

代码:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    >
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

预览:

---

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

Markdown 允许您偷懒，只在硬换行段落的第一行前加上 >。

代码:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

预览:

---

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

块引用可以通过添加额外的 > 级别来嵌套（即块引用中的块引用）。

代码:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

预览:

---

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

---

块引用可以包含其他 Markdown 元素，包括标题、列表和代码块。

代码:

    > ## This is a header.
    >
    > 1.   This is the first list item.
    > 2.   This is the second list item.
    >
    > Here's some example code:
    >
    >     return shell_exec("echo $input | $markdown_script");

预览:

---

> ## This is a header.
>
> 1.  This is the first list item.
> 2.  This is the second list item.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

---

### 列表

Markdown 支持有序（编号）和无序（项目符号）列表。

#### 无序列表

HTML 标签: `<ul>`

无序列表使用**星号（*）**、**加号（+）**和**连字符（-）**。

代码:

    *   Red
    *   Green
    *   Blue

预览:

---

- Red
- Green
- Blue

---

等同于：

代码:

    +   Red
    +   Green
    +   Blue

和：

代码:

    -   Red
    -   Green
    -   Blue

#### 有序列表

HTML 标签: `<ol>`

有序列表使用数字后跟句点：

代码:

    1.  Bird
    2.  McHale
    3.  Parish

预览:

---

1.  Bird
2.  McHale
3.  Parish

---

有可能意外触发有序列表，通过写这样的内容：

代码:

    1986. What a great season.

预览:

---

1986. What a great season.

---

您可以**使用反斜杠转义（\\）**句点：

代码:

    1986\. What a great season.

预览:

---

1986\. What a great season.

---

#### 缩进

##### 块引用

要将块引用放在列表项内，块引用的 > 分隔符需要缩进：

代码:

    *   A list item with a blockquote:
    
        > This is a blockquote
        > inside a list item.

预览:

---

- A list item with a blockquote:

  > This is a blockquote
  > inside a list item.

---

##### 代码块

要将代码块放在列表项内，代码块需要缩进两次 — **8 个空格**或**两个制表符**：

代码:

    *   A list item with a code block:
    
            <code goes here>

预览:

---

- A list item with a code block:

      <code goes here>

---

##### 嵌套列表

代码:

    * A
      * A1
      * A2
    * B
    * C

预览:

---

- A
  - A1
  - A2
- B
- C

---

### 代码块

HTML 标签: `<pre>`

将块的每一行缩进至少**4 个空格**或**1 个制表符**。

代码:

    This is a normal paragraph:
    
        This is a code block.

预览:

---

This is a normal paragraph:

    This is a code block.

---

代码块一直持续到遇到未缩进的行（或文章结尾）。

在代码块内，**& 符号（&）**和角**括号（< 和 >）**会自动转换为 HTML 实体。

代码:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

预览:

---

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

---

以下部分"围栏代码块"和"语法高亮"是扩展功能，您可以使用其他方式编写代码块。

#### 围栏代码块

只需将代码包裹在 ` ``` ` 中（如下所示），您就不需要缩进四个空格。

代码:

    Here's an example:
    
    ```
    function test() {
      console.log("notice the blank line before this function?");
    }
    ```

预览:

---

Here's an example:

```
function test() {
  console.log("notice the blank line before this function?");
}
```

---

#### 语法高亮

在您的围栏块中，添加一个可选的语言标识符，我们将通过语法高亮运行它（[支持的语言](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)）。

代码:

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```

预览:

---

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

---

### 水平分割线

HTML 标签: `<hr />`
将**三个或更多连字符（-）、星号（*）或下划线（_）**单独放在一行上。您可以在连字符或星号之间使用空格。

代码:

    * * *
    ***
    *****
    - - -
    ---------------------------------------
    ___

预览:

---

---

---

---

---

---

---

---

### 表格

HTML 标签: `<table>`

这是一个扩展功能。

用**竖线（|）**分隔列，用**破折号（-）**分隔标题，并使用**冒号（:）**进行对齐。

外部的**竖线（|）**和对齐方式是可选的。每个单元格至少有**3 个分隔符**用于分隔标题。

代码:

```
| Left | Center | Right |
|:-----|:------:|------:|
|aaa   |bbb     |ccc    |
|ddd   |eee     |fff    |

 A | B
---|---
123|456


A |B
--|--
12|45
```

预览:

---

| Left | Center | Right |
| :--- | :----: | ----: |
| aaa  |  bbb   |   ccc |
| ddd  |  eee   |   fff |

| A    | B    |
| ---- | ---- |
| 123  | 456  |

| A    | B    |
| ---- | ---- |
| 12   | 45   |

---

## 行内元素

### 链接

HTML 标签: `<a>`

Markdown 支持两种链接样式：行内和引用。

#### 行内链接

行内链接格式如下：`[链接文本](URL "标题")`

标题是可选的。

代码:

    This is [an example](http://example.com/ "Title") inline link.
    
    [This link](http://example.net/) has no title attribute.

预览:

---

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

---

如果您引用同一服务器上的本地资源，可以使用相对路径：

代码:

    See my [About](/about/) page for details.

预览:

---

See my [About](/about/) page for details.

---

#### 引用链接

您可以预定义链接引用。格式如下：`[id]: URL "标题"`

标题也是可选的。然后您引用链接时，格式如下：`[链接文本][id]`

代码:

    [id]: http://example.com/  "Optional Title Here"
    This is [an example][id] reference-style link.

预览:

---

[id]: http://example.com/ "Optional Title Here"

This is [an example][id] reference-style link.

---

即：

- 包含链接标识符的方括号（**不区分大小写**，可选地使用最多三个空格从左边界缩进）；
- 后跟冒号；
- 后跟一个或多个空格（或制表符）；
- 后跟链接的 URL；
- 链接 URL 可以选择用尖括号包围。
- 可选地后跟链接的标题属性，用双引号或单引号括起来，或用括号括起来。

以下三个链接定义是等效的：

代码:

    [foo]: http://example.com/  "Optional Title Here"
    [foo]: http://example.com/  'Optional Title Here'
    [foo]: http://example.com/  (Optional Title Here)
    [foo]: <http://example.com/>  "Optional Title Here"

使用空的方括号，链接文本本身用作名称。

代码:

    [Google]: http://google.com/
    [Google][]

预览:

---

[Google]: http://google.com/

[Google][]

---

### 强调

HTML 标签: `<em>`, `<strong>`

Markdown 将**星号（*）**和**下划线（_）**视为强调指示符。**单个分隔符**将是 `<em>`；**双分隔符**将是 `<strong>`。

代码:

    *single asterisks*
    
    _single underscores_
    
    **double asterisks**
    
    __double underscores__

预览:

---

_single asterisks_

_single underscores_

**double asterisks**

**double underscores**

---

但是如果您用空格包围 * 或 _，它将被视为字面星号或下划线。

您可以用反斜杠转义它：

代码:

    \*this text is surrounded by literal asterisks\*

预览:

---

\*this text is surrounded by literal asterisks\*

---

### 代码

HTML 标签: `<code>`

用**反引号（`）**包裹它。

代码:

    Use the `printf()` function.

预览:

---

Use the `printf()` function.

---

要在代码跨度中包含字面反引号字符，可以使用**多个反引号**作为开头和结尾分隔符：

代码:

    ``There is a literal backtick (`) here.``

预览:

---

``There is a literal backtick (`) here.``

---

包围代码跨度的反引号分隔符可以包含空格 — 一个在开头后，一个在结尾前。这允许您在代码跨度的开头或结尾放置字面反引号字符：

代码:

    A single backtick in a code span: `` ` ``
    
    A backtick-delimited string in a code span: `` `foo` ``

预览:

---

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``

---

### 图片

HTML 标签: `<img />`

Markdown 使用一种旨在类似于链接语法的图像语法，允许两种样式：行内和引用。

#### 行内图片

行内图像语法如下：`![替代文本](URL "标题")`

标题是可选的。

代码:

    ![Alt text](/path/to/img.jpg)
    
    ![Alt text](/path/to/img.jpg "Optional title")

预览:

---

![Alt text](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp)

![Alt text](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "Optional title")

---

即：

- 一个感叹号：!；
- 后跟一组方括号，包含图像的 alt 属性文本；
- 后跟一组圆括号，包含图像的 URL 或路径，以及一个可选的双引号或单引号括起来的标题属性。

#### 引用图片

引用样式图像语法如下：`![替代文本][id]`

代码:

    [img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp  "Optional title attribute"
    ![Alt text][img id]

预览:

---

[img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "Optional title attribute"

![Alt text][img id]

---

### 删除线

HTML 标签: `<del>`

这是一个扩展功能。

GFM 添加了删除线文本的语法。

代码:

```
~~Mistaken text.~~
```

预览:

---

~~Mistaken text.~~

---

## 其他功能

### 自动链接

Markdown 支持创建 URL 和电子邮件地址"自动"链接的快捷方式：只需用尖括号包围 URL 或电子邮件地址。

代码:

    <http://example.com/>
    
    <address@example.com>

预览:

---

<http://example.com/>

<address@example.com>

---

GFM 会自动链接标准 URL。

代码:

```
https://github.com/emn178/markdown
```

预览:

---

https://github.com/emn178/markdown

---

### 反斜杠转义

Markdown 允许您使用反斜杠转义来生成原本在 Markdown 格式化语法中具有特殊含义的字面字符。

代码:

    \*literal asterisks\*

预览:

---

\*literal asterisks\*

---

Markdown 为以下字符提供反斜杠转义：

代码:

    \   反斜杠
    `   反引号
    *   星号
    _   下划线
    {}  花括号
    []  方括号
    ()  圆括号
    #   井号
    +   加号
    -   减号（连字符）
    .   点
    !   感叹号

## 行内 HTML

对于 Markdown 语法未涵盖的任何标记，您可以直接使用 HTML 本身。无需前缀或分隔符来指示您从 Markdown 切换到 HTML；您只需使用标签。

代码:

    This is a regular paragraph.
    
    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>
    
    This is another regular paragraph.

预览:

---

This is a regular paragraph.

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>


This is another regular paragraph.

---

请注意，Markdown 格式化语法**在块级 HTML 标签内不会被处理**。

与块级 HTML 标签不同，Markdown 语法**在行级标签内会被处理**。

代码:

    <span>**Work**</span>
    
    <div>
        **No Work**
    </div>

预览:

---

<span>**Work**</span>

<div>
  **No Work**
</div>

***