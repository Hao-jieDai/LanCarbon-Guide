---
title: Editing and Formatting
label: codemirror-editor
---

## English

### 1. CodeMirror Editor

#### What changed

The note body is now powered by CodeMirror 6. Markdown markers remain visible because LanCarbon stores your exact source text.

Available editing features:

- Line numbers and active-line highlighting.
- Markdown-aware syntax highlighting and code folding.
- Bracket matching and automatic bracket closing.
- Undo and redo with `Ctrl+Z` and `Ctrl+Shift+Z` or `Ctrl+Y`.
- Search and replace with `Ctrl+F`.
- Indent and outdent with `Tab` and `Shift+Tab`.
- Line wrapping without changing the saved Markdown.
- Chinese IME input and mixed Chinese/English documents.

LanCarbon still autosaves after an edit. The status at the top changes from **Saving…** to **All changes saved**. Switching notes, changing the app theme, restarting, and exporting a Book preserve the exact Markdown text.

#### Useful checks

Try headings, emphasis, a link, a list, a fenced code block and Chinese text. Confirm that Markdown tokens use different colors, the line-number gutter follows the document, and no spelling underline appears.


(edit-and-preview)=
### 2. Edit and Preview

Use the **Edit** and **Preview** buttons in the top toolbar to switch the note body between source editing and rendered output.

- **Edit** shows the CodeMirror Markdown source editor.
- **Preview** parses the current source with the official MyST parser and renders safe HTML.
- Switching modes does not save a second copy, rewrite Markdown, or change the export result.
- The editor instance stays alive while Preview is open, preserving its selection and undo history.
- Preview links are displayed but cannot navigate the Electron window away from LanCarbon.
- Embedded executable HTML and remote images are removed from the in-app preview for security. Asset handling belongs to Phase 3.

The title and tags remain visible in both modes. Statistics continue to count the original Markdown source rather than rendered text.


(myst-syntax)=
### 3. MyST Syntax

Phase 2B previews the common document structures needed for everyday writing:

- Headings, paragraphs, emphasis and strong text.
- Ordered and unordered lists.
- Links, block quotes and horizontal rules.
- Inline code and fenced code blocks.
- Tables and footnotes supported by the MyST parser.
- Standard MyST parsing of the source before HTML rendering.

This is a basic document preview, not the final Jupyter Book website theme. Phase 2C now adds mathematics, directives, roles and within-Book cross-references; see the new reference pages below. The exported project remains the authoritative way to verify full Jupyter Book output.


(formatting-toolbar)=
### 4. Formatting Toolbar

#### Toolbar layout

The formatting toolbar appears below the note title in Edit mode. It writes Markdown into your note; Preview shows the rendered result. The interface uses English and follows Light/Dark mode.

Controls stay on the toolbar whenever their measured widths fit. Resizing the window or changing display scaling moves only the controls that no longer fit into **⋯ (More tools)**. Widening the window restores them. Underline, strikethrough, superscript and subscript keep their U, S, x² and x₂ symbols, with English tooltips.

**Directives** always has its own menu for block content. **⋯** contains other tools only. Abbreviation and Keyboard appear after superscript/subscript when space permits.

#### Everyday writing

| Control | How to use it | Saved Markdown |
| --- | --- | --- |
| Paragraph / Heading 1–6 | Place the cursor in a line or select several lines; choose the level | Heading 1 adds # and a space; changing levels replaces the old prefix |
| Bold / Italic | Select text, then click; click again to remove the formatting | **text** or *text*, with the corresponding markers visible in Edit |
| Underline / Strikethrough | Select text and click U or S | MyST underline/delete roles |
| Superscript / Subscript | Select the characters to raise or lower, then click x² or x₂ | MyST sup/sub roles |
| Lists | Choose Bulleted list or Numbered list; indent/outdent from this menu | List markers and indentation are inserted into the source |
| Quote | Apply to the current or selected lines; click again to remove | Lines begin with > |
| Link | Select text or place the cursor in an existing simple link | A panel asks for Link text and URL |
| Code | Choose Inline code or Code block | Backticks or fenced code; a block panel accepts a language and content |
| Divider | Click at the desired line | A horizontal-rule block is inserted after the line |

With no selection, inline formatting inserts markers and places the cursor between them. To edit links, code blocks, regular tables and simple dollar-delimited formulas, place the cursor inside the existing structure before opening its panel.

#### Apply, cancel and keyboard

- Panel drafts are saved only after **Apply**. **Cancel** or Escape discards the draft and returns to the editor. If a dropdown is open, the first Escape closes that dropdown.
- One toolbar action can be undone in one step with **Ctrl+Z**; **Ctrl+Shift+Z** redoes it.
- **Ctrl+B**, **Ctrl+I** and **Ctrl+K** apply bold, italic and links while editing the body. **Ctrl+F** searches the body. On macOS, use Cmd for the corresponding modifier.
- Spelling underlines are disabled in the editor, search and every input panel. Formula and required-field validation still provide useful errors.
- Special syntax inside code, tables or complex labelled structures may require source editing. A notice explains when an action is unavailable.

#### Quick acceptance

Select Chinese and English text and try the controls. Narrow and widen the window: ordinary controls should reappear as space becomes available, while Directives stays separate. Verify x²/x₂ icons, Apply/Cancel, undo/redo and persistence after restart. Continue with Tables and Mathematics and Directives and Roles.

## 中文

### 1. CodeMirror Editor / 中文

#### 本次变化

笔记正文现在由 CodeMirror 6 驱动。Markdown 标记仍会直接显示，因为 LanCarbon 保存的是用户输入的原始文本。

当前可用的编辑功能：

- 显示行号并突出当前行。
- 根据 Markdown 语法高亮，并支持代码折叠。
- 括号匹配和自动补全括号。
- 使用 `Ctrl+Z` 撤销，使用 `Ctrl+Shift+Z` 或 `Ctrl+Y` 重做。
- 使用 `Ctrl+F` 搜索和替换。
- 使用 `Tab` 和 `Shift+Tab` 增加或减少缩进。
- 自动换行，但不会改变实际保存的 Markdown。
- 支持中文输入法以及中英文混合文档。

编辑后 LanCarbon 仍会自动保存，顶部状态会从 **Saving…** 变为 **All changes saved**。切换笔记、切换应用主题、重启软件以及导出 Book 时，原始 Markdown 都应保持不变。

#### 建议检查

可以输入标题、强调、链接、列表、围栏代码块和中文内容，确认 Markdown 标记呈现不同颜色、行号随正文变化，并且不会出现拼写检查红色下划线。

### 2. Edit and Preview / 中文

使用顶部工具栏中的 **Edit** 和 **Preview** 按钮，可以在 Markdown 源码编辑与渲染结果之间切换。

- **Edit** 显示 CodeMirror Markdown 源码编辑器。
- **Preview** 使用官方 MyST parser 解析当前源码，并输出经过安全清理的 HTML。
- 切换模式不会另存一份内容、改写 Markdown 或改变导出结果。
- 打开 Preview 时编辑器实例仍会保留，因此选区和撤销历史不会丢失。
- 预览会显示链接，但不会允许链接把 Electron 窗口导航到 LanCarbon 之外。
- 为保证安全，应用内预览会删除可执行 HTML 和远程图片；资源管理属于 Phase 3。

标题和标签在两种模式下都保持可见，底部统计继续以原始 Markdown 源码为准，而不是统计渲染后的文字。

### 3. MyST Syntax / 中文

Phase 2B 可以预览日常写作最常用的文档结构：

- 标题、段落、强调和粗体文字。
- 有序列表与无序列表。
- 链接、引用块和水平分隔线。
- 行内代码和围栏代码块。
- MyST parser 支持的表格与脚注。
- 在生成 HTML 前，先按照标准 MyST 规则解析源码。

这里提供的是基础文档预览，并不等同于最终的 Jupyter Book 网站主题。Phase 2C 现已加入数学公式、directive、role 和同 Book 交叉引用，请继续阅读新增参考页面。导出项目并使用官方 CLI 构建，仍然是验证完整 Jupyter Book 输出的权威方式。

### 4. Formatting Toolbar / 中文

#### 工具栏布局

在 Edit 模式下，格式工具栏显示在笔记标题下方。按钮把 Markdown 写入正文，Preview 显示排版结果。界面使用英文，并跟随 Light/Dark 主题。

按钮实际宽度能够放下时就直接显示。缩小窗口或改变显示缩放时，只有放不下的工具才进入 **⋯（More tools）**；扩大窗口后自动恢复。下划线、删除线、上下标保持 U、S、x²、x₂ 图标，悬停显示英文说明。

**Directives** 始终使用独立的块级内容菜单，**⋯** 只收纳其他工具。空间允许时，Abbreviation 和 Keyboard 位于上下标后面。

#### 日常写作

| 控件 | 使用方法 | 写入内容 |
| --- | --- | --- |
| Paragraph / Heading 1–6 | 光标放在当前行或选中多行，再选择级别 | 一级标题生成 # 加空格；切换级别会替换原前缀 |
| Bold / Italic | 选中文字后点击，再次点击可取消 | 加粗或斜体标记，Edit 中保留源码 |
| Underline / Strikethrough | 选中文字，点击 U 或 S | MyST underline/delete 角色 |
| Superscript / Subscript | 选中需要上移或下移的字符，点击 x² 或 x₂ | MyST sup/sub 角色 |
| Lists | 选择无序或有序列表；在菜单中增加或减少缩进 | 列表标记及缩进 |
| Quote | 作用于当前行或选中行，再次点击可取消 | 行首添加 > |
| Link | 选中文字，或把光标放入已有简单链接 | 在面板中填写显示文字和 URL |
| Code | 选择行内代码或代码块 | 行内反引号或代码围栏；代码块可填写语言和正文 |
| Divider | 光标放在目标行再点击 | 在该行后插入水平分隔线 |

未选中文字时，行内格式会插入标记并把光标放在中间。已有链接、代码块、规则表格和普通美元语法公式，可把光标放进去后再次打开对应面板编辑。

#### 应用、取消与快捷键

- 面板草稿只有点击 **Apply** 才保存。**Cancel** 或 Escape 放弃草稿并返回编辑器；若下拉菜单正在展开，第一次 Escape 只关闭菜单。
- 一次工具栏操作可用 **Ctrl+Z** 一次撤销，**Ctrl+Shift+Z** 重做。
- 正文中 **Ctrl+B** 加粗、**Ctrl+I** 斜体、**Ctrl+K** 编辑链接、**Ctrl+F** 搜索；macOS 对应使用 Cmd。
- 正文、搜索和所有输入面板均关闭拼写波浪线；公式语法和必填字段仍进行有效性校验。
- 代码、表格内部或带标签等复杂结构可能需要源码编辑；操作不可用时会给出提示。

#### 快速验收

选中中英文文字试用按钮。缩小再扩大窗口，确认普通工具按可用空间恢复、Directives 独立显示、上下标保持图标。检查 Apply/Cancel、撤销/重做与重启保存。继续阅读 Tables and Mathematics、Directives and Roles。

## Exported Website Theme / 导出网站主题

### Website appearance

LanCarbon exports a rose-colored website theme with every Book. The current page, expanded chapter, page outline, links and references, inline code, keyboard text, code blocks, tables and menus follow the desktop palette. The website's own Light/Dark button switches both palettes. Warning callouts retain the desktop's amber edge.

The export includes lancarbon-theme.css and configures it in myst.yml. Keep this file with the exported Book. Run jupyter book start to preview changes, or jupyter book build --html to rebuild the saved static website. A Python server reads the previously built files; refreshing it alone does not rebuild your Book.

For a newly exported Book, no manual styling is needed. Existing exports must receive the CSS and site.options.style configuration, then be rebuilt. This is website styling; it does not recolor browser tabs or address bars. No remote font or style download is introduced by the LanCarbon theme.

### 网站外观

LanCarbon 导出的每本 Book 都附带玫瑰粉色网站主题。当前页面、展开章节、页内目录、链接与引用、行内代码、按键、代码块、表格和菜单沿用桌面软件的配色。网站自身的 Light/Dark 按钮切换两套色板；警告框保留软件中的琥珀色提示边线。

导出内容包含 lancarbon-theme.css，myst.yml 会自动配置加载它。请将此文件与 Book 一起保留。使用 jupyter book start 预览，或运行 jupyter book build --html 更新已保存的静态网站。Python 服务读取的是上次构建结果，仅刷新网页不会重新构建。

新导出的 Book 无需手工设置。已有导出项目需补充 CSS 和 site.options.style 配置，再重新构建。这是网页内容的样式，不会改变浏览器标签栏或地址栏；LanCarbon 主题不会引入额外的远程字体或样式下载。