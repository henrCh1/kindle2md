# Kindle 转 Markdown

将Kindle HTML笔记本导出转换为标准Markdown格式，包含Obsidian兼容的前置元数据。

## 功能特点

- 将Kindle书籍高亮转换为**标准Markdown**（通用格式）
- 输出包含Obsidian兼容的YAML前置元数据（可在Obsidian中使用，但也支持其他MD编辑器）
- **完整中英文双语支持**
  - 支持 `标注/Highlight` 和 `笔记/Note`
  - 很多开源项目只支持英文，本项目支持中文Kindle导出
- 自动从文件名提取书名

## 安装

1. 克隆本仓库
2. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

## 使用方法

### 作为Python脚本运行

```bash
python kindle_notes_to_md.py -o "output/path/book.md" "path/to/notebook.html"
```

**参数说明：**
- `-o, --output` : 输出文件路径
- `-y, --override` : 覆盖已存在的文件

### 作为Claude Code Skill使用

请参考 [kindle2md-skill](./kindle2md-skill/) 文件夹中的说明进行安装。

## 输出格式

转换后的Markdown包含Obsidian兼容的前置元数据：

```yaml
---
title: 书名
author: 作者
date: 2026-03-20
tags: Books
type: book-note
---

# 高亮与笔记

## 第一章

- 高亮内容
  - *笔记内容*
  - 标注 (黄色) - 位置 123
```

## 如何获取Kindle笔记HTML文件

1. 打开手机上的Kindle应用
2. 找到你的书籍，点击"我的笔记"
3. 点击导出按钮保存为HTML

## 许可证

MIT License
