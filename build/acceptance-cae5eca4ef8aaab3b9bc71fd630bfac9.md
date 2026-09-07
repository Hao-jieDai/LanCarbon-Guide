---
title: Phase 3 Acceptance
label: lancarbon-phase3-acceptance
---

## English

1. Import an image, attachment and UTF-8 .bib file into a disposable Book.
2. Adjust image width, alignment, description and caption; verify both desktop themes and Preview.
3. Insert narrative, parenthetical and grouped citations. Confirm author–year text and References in Preview.
4. Open Citations and confirm Book validation passes. Add a missing key temporarily and confirm validation and export reject it, then correct it.
5. Restart and verify resource references, image settings, bibliography association and citations remain.
6. Export to an empty folder. Confirm myst.yml contains project.bibliography and assets/ contains only required resources.
7. Run jupyter book build --html --strict and check the generated website's images, downloads, citations and bibliography.
8. Test Resources filtering and permanent deletion on disposable data. Confirm references and Book resource settings are removed together.

Phase 3 is accepted when every check passes without changing the original imported files. Attachment reading, executable notebooks, built-in CLI serving and publishing remain later work.

## 中文

1. 在临时 Book 中导入图片、附件和 UTF-8 .bib 文件。
2. 调整图片宽度、对齐、描述和图注，检查两种桌面主题及 Preview。
3. 插入叙述式、括号式和多篇组合引用，检查作者—年份及 References。
4. 在 Citations 确认 Book validation 通过；临时加入缺失引用键，确认校验和导出会阻止，再修正。
5. 重启后检查资源引用、图片设置、文献库关联和引用仍存在。
6. 导出到空目录，确认 myst.yml 包含 project.bibliography，assets/ 只包含所需资源。
7. 运行 jupyter book build --html --strict，检查生成网站的图片、下载、引用和参考文献。
8. 在临时数据上检查 Resources 筛选和永久删除，确认引用及 Book 资源设置同步清除。

全部通过后 Phase 3 验收完成。附件内阅读、可执行 Notebook、内置 CLI 服务和发布仍属于后续工作。

## Resource tools update (1.8.1) / 资源工具更新

Same-name imports now ask: Replace existing updates ALL references to the managed resource; Keep both adds a numbered display name; Cancel imports nothing. Physical filenames remain hashes.

Resources → Show resources separates ordinary Notes from Books. Select one Book, one ordinary note, or Unreferenced; use the checkboxes and Delete selected for a batch. Delete checks references across the entire workspace, including other Books and Book logos, before asking for confirmation. Removing Markdown links retains resources. Confirmed resource deletion removes the managed file permanently; source links are left unchanged and will show missing-resource notices. Shared identical bytes stay on disk while another resource record still needs them. Original imported files and previously exported Books are unaffected. Attachment reading remains a future feature.

同名导入现在弹出三个选项：Replace existing 替换所有原引用使用的资源；Keep both 给新资源显示名添加 (2)、(3) 等序号；Cancel 取消。磁盘继续使用哈希文件名。

Resources → Show resources 区分普通 Notes 和 Books，可选某本书、某篇普通笔记或 Unreferenced（未引用）。勾选资源后点击 Delete selected 批量删除，单个资源也有 Delete。删除提示检查整个工作区的引用，包括其他书籍及书籍图标。仅删除正文链接会保留资源；确认永久删除资源才清除托管文件，正文中的旧链接不会自动改写，会提示资源缺失。若另一条资源记录仍共用相同文件，该文件会保留至最后一条记录被删除。电脑上的原始导入文件和已经导出的 Book 不受影响。软件内附件阅读留待后续开发。