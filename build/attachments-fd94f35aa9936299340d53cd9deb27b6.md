---
title: Attachments and Resource Export
label: lancarbon-phase3-attachments
---

## English

### Attach and manage files

Choose Attach file in Edit to import a PDF, document, spreadsheet or other file (up to 100 MB). Dropping files into the editor also imports them. The Markdown link uses a managed copy; Preview links and Resources → Save a copy let you save the file to another location without launching it automatically.

Resources lists images and attachments across your notes and Books. Search by name, reuse a file with Insert, and expand its reference count to inspect note titles and line numbers. A resource with no references is retained. The checker covers managed Markdown image/link destinations, reference definitions and MyST image/figure arguments; literal code examples are ignored. Missing files are marked in the list.

### Export and move

Export a Book into an empty folder. Referenced resources are copied into assets/, and links in nested pages are adjusted relative to each page. Shared files are copied once; unrelated resources are excluded. The desktop source stays unchanged. Export stops with a message if a required managed file is missing or damaged.

Build with jupyter book build --html --strict, then view the saved website with a local HTTP server. Move the whole exported project, including assets/ and the website theme files. Test an image and an attachment link after moving it.

Data Location migration also copies the resource catalog and files. For backups, keep notes.json, assets.json and assets/ together. Bibliography management remains Phase 3C.

### Acceptance

1. Import an image and a document, then move the original files elsewhere.
2. Restart and verify the image; save an attachment copy and compare it with the original.
3. Reuse a resource on a nested Book page and inspect its references.
4. Export, build, move the export and verify both links again.

## 中文

### 插入和管理附件

在 Edit 点击 Attach file，可导入 PDF、文档、表格等文件，每个不超过 100 MB；也支持拖入编辑区。Markdown 链接引用软件保存的副本。点击 Preview 中的附件链接，或 Resources 中的 Save a copy，可另存文件，不会自动启动附件程序。

Resources 汇总所有笔记和 Book 的图片与附件。可以按名称搜索、点击 Insert 复用，并展开引用次数查看笔记标题和行号。零引用资源仍保留。检查覆盖受管理的 Markdown 图片与链接目标、引用定义和 MyST image/figure 参数，忽略代码示例中的字面引用；缺失文件会明确标注。

### 导出与移动

将 Book 导出到空目录，引用的资源会复制到 assets/，嵌套页面的链接会转换为相对于该页面的路径。共用资源只复制一次，无关资源不导出，软件中的 Markdown 原文保持不变。必要资源缺失或损坏时，导出会停止并提示重新导入。

使用 jupyter book build --html --strict 构建，再通过本地 HTTP 服务查看。移动导出项目时保留整个文件夹，包括 assets/ 和网站主题文件，并重新检查图片及附件链接。

更改 Data Location 时会一起复制资源目录和清单。手动备份需同时保留 notes.json、assets.json 和 assets/。文献管理仍属于后续 Phase 3C。

### 验收

1. 导入一张图片和一个文档，然后移动原文件。
2. 重启检查图片，另存附件副本并与原文件比较。
3. 在 Book 的嵌套页面复用资源，检查引用位置。
4. 导出、构建、移动整个导出目录，再次验证图片和附件。

## Resource tools update (1.8.1) / 资源工具更新

Same-name imports now ask: Replace existing updates ALL references to the managed resource; Keep both adds a numbered display name; Cancel imports nothing. Physical filenames remain hashes.

Resources → Show resources separates ordinary Notes from Books. Select one Book, one ordinary note, or Unreferenced; use the checkboxes and Delete selected for a batch. Delete checks references across the entire workspace, including other Books and Book logos, before asking for confirmation. Removing Markdown links retains resources. Confirmed resource deletion removes the managed file permanently; source links are left unchanged and will show missing-resource notices. Shared identical bytes stay on disk while another resource record still needs them. Original imported files and previously exported Books are unaffected. Attachment reading remains a future feature.

同名导入现在弹出三个选项：Replace existing 替换所有原引用使用的资源；Keep both 给新资源显示名添加 (2)、(3) 等序号；Cancel 取消。磁盘继续使用哈希文件名。

Resources → Show resources 区分普通 Notes 和 Books，可选某本书、某篇普通笔记或 Unreferenced（未引用）。勾选资源后点击 Delete selected 批量删除，单个资源也有 Delete。删除提示检查整个工作区的引用，包括其他书籍及书籍图标。仅删除正文链接会保留资源；确认永久删除资源才清除托管文件，正文中的旧链接不会自动改写，会提示资源缺失。若另一条资源记录仍共用相同文件，该文件会保留至最后一条记录被删除。电脑上的原始导入文件和已经导出的 Book 不受影响。软件内附件阅读留待后续开发。

## Deletion update (1.8.2) / 删除行为更新

From 1.8.2, confirming resource deletion also removes its image/link occurrences and image/figure blocks from ALL Notes and Books, and clears matching Book logos/favicons. Surrounding prose and literal code examples remain. This supersedes the 1.8.1 behavior described above. Removing only a link still keeps the resource.

从 1.8.2 起，确认删除资源会同时移除所有笔记和 Book 中对应的图片、附件链接和 image/figure 图片块，并清除对应的书籍图标设置；周围正文和代码示例保留。此规则取代上文 1.8.1 的旧删除行为。仅删除正文引用仍保留资源文件。

<!-- phase-3-acceptance-attachment -->
## Acceptance attachment / 验收附件

[LanCarbon Phase 3 Acceptance Checklist.txt](../../assets/a662bf30fc2e013c6e1dec881dbe312716b338784ca4b3662bb93e78f8dbfc1f.txt)
