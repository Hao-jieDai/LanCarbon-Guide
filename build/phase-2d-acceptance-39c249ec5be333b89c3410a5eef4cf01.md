---
title: Phase 2 Acceptance
label: phase-2d-acceptance
---

## English

### 1. Phase 2D Acceptance

Phase 2D packages and verifies the complete Phase 2. It does not introduce Phase 3 assets or bibliography management.

1. Back up your workspace using the folder shown by Data Location. Close LanCarbon and install this release over the previous version; do not uninstall or remove your data.
2. Confirm ReadMe shows the new release and this Book retains your original Getting Started and Phase 1 Reference pages. New reference pages should appear exactly once; user-edited pages must not be overwritten.
3. Repeat the Phase 2A/2B checks: old notes and ReadMe visible in Edit, real Chinese IME, multiple Enter presses, search, undo/redo, persistent view mode and long-document scrolling.
4. Complete the Phase 2C checklist below. Wait for All changes saved, restart, and verify the source and Book structure.
5. Export this Book into an empty directory. Run jupyter book build --html --strict. Then run jupyter book start and keep the terminal open while visiting the printed localhost URL. Stop it with Ctrl+C after checking.
6. Test new/delete/pin/search, Book pages and tree dragging on disposable content. Confirm editing continues immediately after deletion.

Official CLI validation may need internet to download book-theme; this does not mean LanCarbon's local preview needs internet. If downloads fail, resolve the network/proxy problem and retry without changing your Markdown. Phase 2 is accepted only after you approve these checks.

(phase-2a-acceptance)=
### 2. Phase 2A Acceptance

Use this checklist to accept Phase 2A:

1. Open this page and confirm that line numbers and Markdown syntax colors are visible.
2. Create a normal Note and enter Chinese and English text with an IME.
3. Add several Markdown headings, lists, links, brackets and a fenced code block.
4. Test `Tab`, `Shift+Tab`, `Ctrl+Z`, redo and `Ctrl+F` inside the body editor.
5. Switch between Light and Dark themes and confirm the editor changes without losing the cursor or content.
6. Wait for **All changes saved**, switch to another note, return, and confirm the exact text remains.
7. Restart LanCarbon and confirm the edited Note and Book pages are restored.
8. Export this Book to an empty directory and run `jupyter book build --html --strict` to confirm Phase 1 export still works.

Phase 2A is accepted when all checks pass. Preview is covered by the Phase 2B and Phase 2C checks below.


(phase-2b-acceptance)=
### 3. Phase 2B Acceptance

1. Open a Note containing headings, lists, emphasis, a link, a quote, a table and a fenced code block.
2. Select **Preview** and confirm each structure renders as formatted content rather than visible Markdown markers.
3. Select **Edit** and confirm the exact original source and undo history remain available.
4. Edit the source, open Preview again, and confirm the result updates immediately.
5. Click an external link and confirm it does not navigate the app; internal Book links should open their target.
6. Switch Light/Dark themes in both modes and confirm all text remains readable.
7. Restart the app and confirm the saved source remains unchanged.
8. Export the Book and run `jupyter book build --html --strict` to verify Phase 1 compatibility.

Phase 2B is accepted when this checklist and the Phase 2A checklist both pass.


(phase-2c-acceptance)=
### 4. Phase 2C Acceptance

1. Open Tables and Mathematics in Preview. Confirm inline, block and role mathematics, fractions, symbols, offline fonts and equation numbers.
2. Open Directives and Roles. Confirm nested callouts, a custom warning title, an expandable dropdown, abbreviations, sub/superscripts and keyboard text.
3. Open Cross References. Click each local/page/equation reference; confirm the right page and target open without leaving Preview.
4. In a disposable page, add an unknown directive, an invalid formula and a missing label. Confirm Preview notices and visible fallback text. Fix the source and confirm the notices disappear.
5. Rename a target page title without changing its Export Path. Confirm file links still work. Change a label deliberately and confirm old label references become unresolved.
6. Switch between light/dark, Edit/Preview and other pages. Confirm readability, intact Markdown and normal editing. No network is needed for these steps.

## 中文

### 1. Phase 2D Acceptance / 中文

Phase 2D 负责完整 Phase 2 的测试和交付，不提前实现 Phase 3 的资源或文献管理。

1. 根据 Data Location 显示的目录备份工作区；关闭 LanCarbon 后直接覆盖安装，不卸载或删除数据。
2. 确认 ReadMe 显示新版本，Book 中原有 Getting Started 和 Phase 1 Reference 保持不变；新教程只增加一次，用户修改过的页面不能被覆盖。
3. 重新检查 Phase 2A/2B：旧笔记和 ReadMe 在 Edit 可见，真实中文输入法、多次回车、搜索、撤销/重做、模式保持和长文滚动正常。
4. 完成下方 Phase 2C 清单。等待 All changes saved 后重启，确认源码和 Book 结构恢复正常。
5. 导出本 Book 到空目录，运行 jupyter book build --html --strict；再运行 jupyter book start，保持终端打开并访问输出的 localhost 地址。检查后使用 Ctrl+C 停止服务。
6. 用可删除内容检查新建/删除/置顶/搜索、Book 页面和目录拖拽，删除后应能立即继续编辑。

官方 CLI 可能需要联网下载 book-theme，这不意味着 LanCarbon 的本地预览需要网络。如果下载失败，请排查网络/代理后重试，不要因此改写 Markdown。Phase 2 只有在你确认上述检查后才算验收完成。

### 2. Phase 2A Acceptance / 中文

请按以下步骤验收 Phase 2A：

1. 打开本页面，确认正文左侧显示行号，并且 Markdown 语法具有不同颜色。
2. 新建普通 Note，使用中文输入法输入中英文混合内容。
3. 输入多个 Markdown 标题、列表、链接、括号和围栏代码块。
4. 在正文编辑器中测试 `Tab`、`Shift+Tab`、`Ctrl+Z`、重做和 `Ctrl+F`。
5. 在 Light 与 Dark 主题之间切换，确认编辑器随之变化，并且光标和正文不会丢失。
6. 等待顶部显示 **All changes saved**，切换到其他笔记后再返回，确认文本完全一致。
7. 重启 LanCarbon，确认修改后的普通 Note 和 Book 页面都能恢复。
8. 将本 Book 导出到空目录，并运行 `jupyter book build --html --strict`，确认 Phase 1 导出功能没有回归。

以上检查全部通过即可验收 Phase 2A。Preview 由下方 Phase 2B 与 Phase 2C 清单覆盖。

### 3. Phase 2B Acceptance / 中文

1. 打开一篇包含标题、列表、强调、链接、引用、表格和围栏代码块的 Note。
2. 点击 **Preview**，确认各种结构显示为格式化内容，而不是直接显示 Markdown 标记。
3. 点击 **Edit**，确认原始源码完全一致，且撤销历史仍然可用。
4. 修改源码后再次打开 Preview，确认渲染结果立即更新。
5. 点击外部链接，确认不会导航应用窗口；Book 内部链接则应打开正确目标。
6. 在两种模式下切换 Light/Dark 主题，确认所有文字都清晰可读。
7. 重启应用，确认保存的源码没有发生变化。
8. 导出 Book 并运行 `jupyter book build --html --strict`，确认 Phase 1 兼容性。

本清单和 Phase 2A 清单全部通过，即可验收 Phase 2B。

### 4. Phase 2C Acceptance / 中文

1. 在 Preview 打开 Tables and Mathematics，检查行内公式、公式块、math role、分式、符号、离线字体和编号。
2. 打开 Directives and Roles，检查嵌套提示块、自定义 warning 标题、可展开的 dropdown、缩写、上下标和按键文字。
3. 打开 Cross References，逐个点击本页、跨页和公式引用，确认打开正确页面并定位目标，且始终保持 Preview。
4. 新建一篇可删除的测试页，加入未知 directive、错误公式和不存在的 label。确认 Preview notices 和回退原文可见；修正源码后提示应消失。
5. 修改目标页面标题，但不要修改 Export Path，确认文件路径链接仍然有效；故意修改 label，确认旧 label 引用变为无法解析。
6. 切换浅/深主题、Edit/Preview 和其他页面，确认可读性、源码完整性以及编辑正常。以上操作均不需要联网。