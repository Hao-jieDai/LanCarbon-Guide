---
title: Book Settings
short_title: Book Settings
description: An explanation of every Book Settings field.
date: 2026-09-02
keywords:
  - book settings
  - title
  - authors
  - license
  - GitHub
  - logo
  - favicon
label: book-settings
---

## English

Book Settings describe the complete Book and generated website.

The `(*)` marker is a recommendation. It helps identify important fields but does not prevent saving an incomplete draft.

### Book title (*)

The formal title of the Book.

It is written to `project.title` in `myst.yml`. If it is empty during export, LanCarbon uses `Untitled Book`.

Example: `LanCarbon Guide`

### Subtitle

An optional secondary title.

Example: `A Guide to Notes and Jupyter Book 2`

### Description

A summary of the complete Book. It can be used by templates, search systems and publishing platforms.

### Authors

The default authors of the complete Book.

Separate multiple authors with commas:

`Haojie Dai, Jane Smith`

Using a full name is recommended because MyST may warn when it cannot distinguish the given name and family name.

### GitHub repository URL

The address of the GitHub repository associated with the Book.

Example:

`https://github.com/example/lancarbon-guide`

This field does not create a repository, upload files or publish the Book automatically.

### License

The license that describes how the content may be reused.

Examples:

- `CC-BY-4.0` for openly licensed written content
- `MIT` for software-oriented projects

Choose a license only after confirming that it matches the intended use.

### Keywords

Project-level search terms. Separate multiple keywords with commas.

Example:

`LanCarbon, Jupyter Book, MyST, Markdown`

### Site title

The title displayed by the generated website.

If it is empty, LanCarbon uses the Book title.

### Logo Path

A relative path to the website logo.

Example:

`images/logo.png`

Phase 1 does not copy the image automatically. The file must exist at that path in the exported project.

### Favicon Path

A relative path to the browser tab icon.

Example:

`images/favicon.ico`

Phase 1 does not copy the favicon automatically. Leave this field empty unless the file will be added manually after export.

---

## 中文

Book Settings 用来描述整本 Book 和最终生成的网站。

`(*)` 是建议标记，用来提醒哪些字段比较重要，但不会阻止保存尚未完成的草稿。

### Book title (*)

Book 的正式标题。

该字段会写入 `myst.yml` 的 `project.title`。如果导出时为空，LanCarbon 会使用 `Untitled Book`。

示例：`LanCarbon Guide`

### Subtitle

可选的副标题。

示例：`A Guide to Notes and Jupyter Book 2`

### Description

整本 Book 的摘要。网站模板、搜索系统和发布平台可以使用该信息。

### Authors

整本 Book 的默认作者。

多个作者使用逗号分隔：

`Haojie Dai, Jane Smith`

建议填写完整姓名，因为只有一个名称时，MyST 可能无法区分名和姓并给出警告。

### GitHub repository URL

与当前 Book 对应的 GitHub 仓库地址。

示例：

`https://github.com/example/lancarbon-guide`

该字段不会自动创建仓库、上传文件或发布 Book。

### License

说明内容如何被他人使用的许可证。

示例：

- `CC-BY-4.0`：适合开放授权的文字内容
- `MIT`：适合偏软件性质的项目

请在确认许可证符合实际用途后再填写。

### Keywords

整本项目的关键词。多个关键词使用逗号分隔。

示例：

`LanCarbon, Jupyter Book, MyST, Markdown`

### Site title

生成网站后显示的网站名称。

如果留空，LanCarbon 会使用 Book title。

### Logo Path

网站 Logo 的相对路径。

示例：

`images/logo.png`

Phase 1 不会自动复制图片，导出项目中必须存在这个文件。

### Favicon Path

浏览器标签页图标的相对路径。

示例：

`images/favicon.ico`

Phase 1 不会自动复制 favicon。如果不准备手动添加文件，应当将此字段留空。