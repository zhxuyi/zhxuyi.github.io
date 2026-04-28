---
layout: post
title: "Markdown 写作语法速查"
date: 2024-02-01 10:00:00 +0800
categories: [技术]
tags: [Markdown, 写作]
---

Markdown 是一种轻量级标记语言，用简洁的符号表示格式，既方便书写，又能被工具渲染成好看的 HTML。

这篇文章汇总了常用的 Markdown 语法，方便随时查阅。

## 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
```

## 强调

```markdown
**粗体文本**
*斜体文本*
~~删除线~~
```

效果：**粗体文本**，*斜体文本*，~~删除线~~

## 列表

无序列表：

```markdown
- 苹果
- 香蕉
- 橙子
```

有序列表：

```markdown
1. 第一步
2. 第二步
3. 第三步
```

## 链接与图片

```markdown
[链接文字](https://example.com)
![图片描述](图片URL)
```

## 引用

```markdown
> 这是一段引用文字。
```

> 这是一段引用文字。

## 代码

行内代码：`` `code` ``

代码块（指定语言可高亮）：

````markdown
```python
def hello():
    print("Hello, World!")
```
````

```python
def hello():
    print("Hello, World!")
```

## 表格

```markdown
| 列1 | 列2 | 列3 |
|-----|-----|-----|
| A   | B   | C   |
| D   | E   | F   |
```

| 列1 | 列2 | 列3 |
|-----|-----|-----|
| A   | B   | C   |
| D   | E   | F   |

## 分隔线

```markdown
---
```

---

掌握以上这些，日常写作已经绰绰有余。Markdown 的哲学是"所写即所见"——让格式服务于内容，而不是喧宾夺主。
