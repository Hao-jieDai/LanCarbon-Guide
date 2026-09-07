---
title: Page Properties
short_title: Page Properties
description: An explanation of every Page Properties field.
date: 2026-09-02
keywords:
  - page properties
  - export path
  - label
  - frontmatter
  - authors
label: page-properties
---

## English

Page Properties describe an individual page.

The page title is edited in the main editor. Other metadata is configured through **Page Properties**.

### Export Path (*)

The relative Markdown path generated inside the exported project.

Examples:

- `guide/getting-started/index.md`
- `guide/phase-1/page-properties.md`

Rules:

- Use forward slashes `/`.
- Do not use an absolute Windows path.
- Do not use `..`.
- Avoid spaces and reserved Windows names.
- Every page should use a unique path.
- The home page is always `index.md`.

Renaming or moving a page does not automatically change its Export Path. This protects existing links.

If a non-home page has an empty Export Path, LanCarbon generates a stable fallback path from its page ID.

### Show in table of contents

Controls whether the page is visible in website navigation.

When disabled:

- The Markdown file is still exported.
- The page is still built.
- Other pages can still link to it.
- The TOC entry uses `hidden: true`.

### Short title

An optional shorter title for navigation or compact layouts.

Example:

Full title: `Understanding Book Settings`

Short title: `Book Settings`

### Description

A summary of the individual page.

### Authors

Authors responsible for this page.

Leave this empty when the page uses the Book-level authors. Fill it when a page has different authors.

### Date

The publication or revision date of the page.

The interface uses the `YYYY-MM-DD` format.

Example: `2026-09-02`

### Keywords

Search terms describing the individual page. Separate multiple values with commas.

### Label

A stable identifier used by MyST cross-references.

Recommended format:

- Lowercase English letters
- Numbers when necessary
- Hyphens between words
- No spaces
- Unique within the Book

Example:

`page-properties`

A label should describe the page’s meaning rather than its current directory position.

---

## 中文

Page Properties 用来描述单个页面。

页面标题在主编辑器中修改，其他页面元数据通过 **Page Properties** 设置。

### Export Path (*)

页面在导出项目中生成的相对 Markdown 路径。

示例：

- `guide/getting-started/index.md`
- `guide/phase-1/page-properties.md`

规则：

- 使用正斜杠 `/`。
- 不要填写 Windows 绝对路径。
- 不要使用 `..`。
- 避免空格和 Windows 保留名称。
- 每个页面应使用唯一的路径。
- 首页始终为 `index.md`。

重命名或拖动页面不会自动改变 Export Path，从而避免已有链接失效。

如果非首页页面的 Export Path 为空，LanCarbon 会根据页面 ID 生成稳定的回退路径。

### Show in table of contents

控制页面是否显示在网站导航目录中。

关闭后：

- Markdown 文件仍会导出。
- 页面仍会参与构建。
- 其他页面仍然可以链接到它。
- 对应的 TOC 项会使用 `hidden: true`。

### Short title

可选的短标题，适合导航栏或空间较小的界面。

示例：

完整标题：`Understanding Book Settings`

短标题：`Book Settings`

### Description

当前页面的摘要。

### Authors

负责当前页面的作者。

页面沿用整本 Book 的作者时可以留空。只有页面作者与 Book 默认作者不同时才需要填写。

### Date

页面的发布日期或修订日期。

界面使用 `YYYY-MM-DD` 格式。

示例：`2026-09-02`

### Keywords

描述当前页面的关键词。多个关键词使用逗号分隔。

### Label

MyST 跨页面引用所使用的稳定标识符。

推荐格式：

- 使用小写英文字母
- 必要时可以包含数字
- 单词之间使用连字符
- 不使用空格
- 在整本 Book 中保持唯一

示例：

`page-properties`

Label 应描述页面含义，而不是当前目录位置。