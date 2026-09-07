---
title: Citations and Bibliographies
label: lancarbon-phase3-citations
---


### Import and cite

Open a Book page in Edit and choose Citations. Import a UTF-8 BibTeX .bib file (up to 5 MB). The library is stored as a managed hashed resource and associated with this Book. Search by author, title, year or citation key, select one or more entries, then insert a parenthetical citation. A single entry can also be inserted as a narrative citation.

LanCarbon writes standard MyST/Pandoc syntax: `@key` for narrative citations and `[@key; @other]` for grouped parenthetical citations. Preview shows author–year text and the page's cited references. Removing a library from a Book keeps its managed resource; deleting it in Resources removes the Book association.

### Export

Export adds the managed .bib path to project.bibliography in myst.yml and copies the source into assets/. Missing or duplicate citation keys stop export. The official Jupyter Book build produces the final citations and bibliography.



### 导入与引用

在 Book 页面 Edit 模式点击 Citations，导入 UTF-8 BibTeX .bib 文件（不超过 5 MB）。文献库作为哈希命名的受管理资源保存，并关联当前 Book。可按作者、标题、年份或引用键搜索；选择一项或多项后插入括号式引用，单项也可插入叙述式引用。

LanCarbon 写入标准 MyST/Pandoc 语法：叙述式为 `@key`，多篇括号式为 `[@key; @other]`。Preview 显示作者—年份和当前页面引用的参考文献。从 Book 移除文献库不会删除资源；在 Resources 删除资源则会清除 Book 关联。

### 导出

导出时会在 myst.yml 的 project.bibliography 写入受管理 .bib 路径，并把源文件复制到 assets/。引用键缺失或重复时阻止导出；最终引用和参考文献格式以官方 Jupyter Book 构建为准。

## Resource tools update (1.8.1) / 资源工具更新

Same-name imports now ask: Replace existing updates ALL references to the managed resource; Keep both adds a numbered display name; Cancel imports nothing. Physical filenames remain hashes.

Resources → Show resources separates ordinary Notes from Books. Select one Book, one ordinary note, or Unreferenced; use the checkboxes and Delete selected for a batch. Delete checks references across the entire workspace, including other Books and Book logos, before asking for confirmation. Removing Markdown links retains resources. Confirmed resource deletion removes the managed file permanently; source links are left unchanged and will show missing-resource notices. Shared identical bytes stay on disk while another resource record still needs them. Original imported files and previously exported Books are unaffected. Attachment reading remains a future feature.

同名导入现在弹出三个选项：Replace existing 替换所有原引用使用的资源；Keep both 给新资源显示名添加 (2)、(3) 等序号；Cancel 取消。磁盘继续使用哈希文件名。

Resources → Show resources 区分普通 Notes 和 Books，可选某本书、某篇普通笔记或 Unreferenced（未引用）。勾选资源后点击 Delete selected 批量删除，单个资源也有 Delete。删除提示检查整个工作区的引用，包括其他书籍及书籍图标。仅删除正文链接会保留资源；确认永久删除资源才清除托管文件，正文中的旧链接不会自动改写，会提示资源缺失。若另一条资源记录仍共用相同文件，该文件会保留至最后一条记录被删除。电脑上的原始导入文件和已经导出的 Book 不受影响。软件内附件阅读留待后续开发。