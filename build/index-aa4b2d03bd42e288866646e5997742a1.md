---
title: Phase 1 Reference
description: guide/phase-1/index.md
date: 2026-09-02
keywords:
  - phase 1
  - export
  - workspace
  - MyST
  - Jupyter Book
label: phase-1-reference
---

## English

Phase 1 establishes the data model, Book hierarchy and standard Jupyter Book 2 export workflow.

### Implemented features

#### Local workspace

- Notes and Books are stored in a local Workspace v2 file.
- Existing Workspace v1 Notes are migrated without rewriting their Markdown.
- Data is saved automatically.
- The data location can be viewed and changed.
- Existing data is copied and verified before switching locations.

#### Book organization

- Multiple Books can be created.
- Each Book has one fixed home page.
- A Note can belong to no more than one Book.
- Sections and Child Pages are real pages.
- Pages can contain additional child pages.
- Every page except the home page can be reordered.
- Removing a page from a Book preserves its content.
- Deleting a page or Book permanently deletes the corresponding content.

#### Export

- Export is only allowed to a selected empty directory.
- Existing files are never overwritten.
- LanCarbon generates `myst.yml`.
- LanCarbon generates one Markdown file for every Book page.
- LanCarbon generates an export `README.md`.
- The directory structure follows each page’s stable Export Path.
- Existing YAML frontmatter is merged with Page Properties.
- Internal LanCarbon IDs, timestamps and interface state are not exported.
- Hidden pages use `hidden: true` in the MyST table of contents.

### Not included in Phase 1

Phase 1 does not include:

- Rendered Markdown or MyST preview
- CodeMirror editing
- Notebook editing
- Image and resource copying
- BibTeX and citation management
- Advanced validation
- Built-in Jupyter Book process management
- GitHub Pages initialization

These features belong to later development phases.

---

## 中文

Phase 1 建立了工作区数据模型、Book 目录结构和标准 Jupyter Book 2 导出流程。

### 已实现功能

#### 本地工作区

- Notes 和 Books 保存在本机 Workspace v2 文件中。
- 旧版 Workspace v1 Notes 会无损迁移，不会改写原始 Markdown。
- 编辑内容会自动保存。
- 可以查看和修改数据目录。
- 切换目录前会复制并校验已有数据。

#### Book 组织

- 可以创建多个 Book。
- 每个 Book 都有一个固定首页。
- 同一篇 Note 最多属于一个 Book。
- Section 和 Child Page 都是真实页面。
- 页面可以继续包含下一层子页面。
- 除首页外，所有页面都可以重新排序。
- 从 Book 移除页面时会保留内容。
- 删除页面或 Book 时会永久删除对应内容。

#### 导出

- 只能导出到用户选择的空目录。
- 不会覆盖已有文件。
- LanCarbon 会生成 `myst.yml`。
- Book 中的每个页面都会生成对应的 Markdown 文件。
- LanCarbon 会生成导出说明 `README.md`。
- 文件目录遵循页面稳定的 Export Path。
- 原有 YAML frontmatter 会与 Page Properties 合并。
- LanCarbon 内部 ID、时间戳和界面状态不会被导出。
- 隐藏页面会在 MyST 目录中使用 `hidden: true`。

### Phase 1 尚未包含

Phase 1 尚未实现：

- Markdown 或 MyST 渲染预览
- CodeMirror 编辑器
- Notebook 编辑
- 图片和资源复制
- BibTeX 和引用管理
- 进阶校验
- 软件内置的 Jupyter Book 进程管理
- GitHub Pages 初始化

这些功能属于后续开发阶段。