# Kindle to Markdown

Convert Kindle HTML notebook exports to Markdown format with Obsidian-compatible frontmatter.

## Features

- Convert Kindle book highlights to **standard Markdown** (通用格式)
- Output with Obsidian-compatible YAML frontmatter (可在Obsidian中使用，但也支持其他MD编辑器)
- **Full bilingual support**: English and Chinese
  - Supports both `标注/Highlight` and `笔记/Note`
  - Many open source projects only support English, this one works with Chinese Kindle exports
- Auto-extract book title from filename

## Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### As a Python Script

```bash
python kindle_notes_to_md.py -o "output/path/book.md" "path/to/notebook.html"
```

**Options:**
- `-o, --output` : Output file path
- `-y, --override` : Override existing file

### As a Claude Code Skill

See [kindle2md-skill](./kindle2md-skill/) folder for skill installation.

## Output Format

The converted Markdown includes Obsidian-compatible frontmatter:

```yaml
---
title: Book Title
author: Author Name
date: 2026-03-20
tags: Books
type: book-note
---

# Raw Highlights & Notes

## Chapter 1

- Highlight text here
  - *Note text here*
  - 标注 (黄色) - 位置 123
```

## Get Kindle Notes in HTML

1. Open the Kindle app on your phone
2. Find your book and go to "My Notebook"
3. Tap the export button to save as HTML

## License

MIT License
