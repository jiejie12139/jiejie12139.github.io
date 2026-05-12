---
layout: post
title:  "Jekyll 博客测试：本地环境与 Markdown 示例"
date:   2026-05-12 14:30:00 +0800
categories: jekyll update test
tags: [Jekyll, 测试, Markdown, 本地部署]
---

## 📌 测试目的

这篇文章主要用于验证 Jekyll 本地网站是否搭建成功，以及 Markdown 渲染、代码高亮、分类标签等功能是否正常工作。
本网站及其资源仅供学习交流使用，请在下载后48h内删除

**测试日期：** 2026年5月12日  
**测试环境：** Windows + Ruby + Jekyll 4.4.1

---

## ✅ 基础渲染测试

### 文本样式

- **粗体文本**
- *斜体文本*
- ***粗斜体***
- ~~删除线~~
- 行内代码：`bundle exec jekyll serve`

### 引用块

> Jekyll 是一个简单的、博客感知的静态网站生成器。它接受 Markdown 或 Textile 文件，利用布局、模板和 Liquid 代码，生成完整的静态网站。

---

## 🔧 代码高亮测试

### Ruby 代码（Jekyll 相关）

```ruby
# 这是一个简单的 Jekyll 插件示例
module Jekyll
  class TestTag < Liquid::Tag
    def render(context)
      "Hello from Jekyll plugin!"
    end
  end
end

Liquid::Template.register_tag('test', Jekyll::TestTag)