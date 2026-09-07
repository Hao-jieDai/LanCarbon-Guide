---
title: Directives and Roles
label: phase-2-directives
---

## English

### 1. Directives and Roles

Directives are blocks; roles are inline. Use three backticks or colons around a directive. Use a longer outer fence for nesting. Common callouts include note, tip, warning, important, caution and admonition.

::::{note}
This is a **note** with nested content.

:::{tip}
Keep the original Markdown editable.
:::
::::

:::{warning} Check your source
A warning is visible without changing the saved text.
:::

:::{dropdown} Open this example
You can expand this block with the mouse or keyboard.
:::

Roles: {abbr}`CO2 (Carbon dioxide)`, H{sub}`2`O, x{sup}`2`, {kbd}`Ctrl+F`, {underline}`underlined`, {smallcaps}`Small Capitals`.

Unknown directives/roles remain visible with a Preview notice. File includes, embedded programs, diagrams and remote images are not executed or downloaded. Some official CLI plugins provide additional syntax that is not available in this local preview.

(toolbar-roles-directives)=
### 2. Inline Roles and Directive Panels

#### Abbreviation and Keyboard

**Abbreviation:** select an acronym such as IPCC and click Abbreviation. Fill **Full meaning** and Apply. With no selection, enter both fields. Preview shows the abbreviation, with its explanation on hover. A simple existing abbreviation can be reopened from the source.

~~~markdown
{abbr}`IPCC (Intergovernmental Panel on Climate Change)`
~~~

**Keyboard:** select Ctrl+F and click Keyboard to format it immediately; with no selection, a panel asks for the key combination. This only styles text and does not assign or execute a shortcut. The source uses a kbd role:

~~~markdown
{kbd}`Ctrl+F`
~~~

Both roles use a single line. The panels reject backticks that would break the role syntax. Use the U, S, x² and x₂ controls for underline, strikethrough, superscript and subscript respectively.

#### Directives menu

| Entry | What the panel creates |
| --- | --- |
| Note | Information block, optional custom title |
| Tip | Helpful suggestion, optional custom title |
| Important | Important information, optional custom title |
| Warning | Warning block, optional custom title |
| Caution | Caution block, optional custom title |
| Admonition | General callout with a required custom title |
| Nested blocks | Outer and inner blocks, each with type, title and content |
| Dropdown | Required title; content starts collapsed |
| Initially open | Required title; content starts expanded and can be collapsed |

Select ordinary prose to bring it into the panel, or place the cursor at an insertion point. Write Markdown in **Content**, then Apply. Titles must stay on one line. In Nested blocks, choose each layer's type; custom Admonition layers require titles. The application generates longer outer fences so nested blocks remain contained.

Initially open is a preset using an admonition with dropdown and open options:

~~~markdown
:::{admonition} Details
:class: dropdown
:open: true

This content starts expanded.
:::
~~~

Custom warning and Initially open are display choices/titles, not additional directive names. After inserting a block, continue editing its source. The dedicated Directives menu stays available even when other tools move into ⋯.

#### Acceptance

Create an abbreviation and hover over it in Preview. Format Ctrl+F as Keyboard. Try every Directives entry, including an outer Note with an inner Tip. Check the custom title appears once, Dropdown starts closed and Initially open starts open. Cancel an unused draft, undo an insertion and restart to verify persistence. Export the Book and verify these examples with Jupyter Book as well.

## 中文

### 1. Directives and Roles / 中文

directive 用于整块内容，role 用于行内内容。directive 外层可使用三个反引号或冒号；嵌套时外层围栏应比内层长。常用提示块包括 note、tip、warning、important、caution 和 admonition。

上面先展示 note 中嵌套 tip，然后展示带自定义标题的 warning，最后是 dropdown 折叠块。展开 Open this example，确认可以看到折叠正文。所有格式只影响预览，不会改变保存的源码。

行内示例依次展示：带完整名称提示的 CO2 缩写、水分子下标、平方上标、Ctrl+F 按键、下划线以及小型大写字母。切换 Edit 可查看每个 role 的完整语法。

未知 directive/role 会保留可见内容并显示 Preview notice。软件不会执行文件 include、嵌入程序、图表程序，也不会下载远程图片。官方 CLI 的部分插件扩展语法可能不在本地预览支持范围内。

### 2. Inline Roles and Directive Panels / 中文

#### 缩写与按键

**Abbreviation**：选中 IPCC 等缩写并点击按钮，在 **Full meaning** 中填写完整解释后 Apply；没有选区时填写两个字段。Preview 中显示缩写，悬停可查看解释。普通已有缩写可从源码中重新打开面板。

~~~markdown
{abbr}`IPCC (Intergovernmental Panel on Climate Change)`
~~~

**Keyboard**：选中 Ctrl+F 并点击按钮即可直接添加按键样式；没有选区时弹出填写面板。该功能只改变文字显示，不注册或执行快捷键，生成 kbd 行内角色：

~~~markdown
{kbd}`Ctrl+F`
~~~

两种角色都使用单行内容；面板会拒绝破坏语法的反引号。下划线、删除线、上下标分别使用 U、S、x²、x₂ 控件。

#### Directives 菜单

| 入口 | 面板生成的内容 |
| --- | --- |
| Note | 说明框，可选自定义标题 |
| Tip | 提示框，可选自定义标题 |
| Important | 重要信息框，可选自定义标题 |
| Warning | 警告框，可选自定义标题 |
| Caution | 注意事项框，可选自定义标题 |
| Admonition | 通用提示框，必须填写自定义标题 |
| Nested blocks | 嵌套块，可分别设置内外层类型、标题和正文 |
| Dropdown | 必填标题，正文默认收起 |
| Initially open | 必填标题，正文默认展开且可以收起 |

可以先选中普通正文带入面板，或把光标放在插入位置。在 **Content** 中填写 Markdown，再点击 Apply；标题保持单行。Nested blocks 分别选择内外层类型，选择 Admonition 的层级需要标题。软件自动生成更长的外层围栏，使嵌套关系正确。

Initially open 是通过 admonition、dropdown 和 open 选项实现的预设：

~~~markdown
:::{admonition} 详情
:class: dropdown
:open: true

这段内容默认展开。
:::
~~~

Custom warning、Initially open 是显示方式或示例标题，不是额外的底层指令名称。块插入后继续通过源码编辑；即使其他工具进入 ⋯，Directives 也保持独立可用。

#### 验收

创建缩写并在 Preview 悬停查看解释，为 Ctrl+F 添加按键样式。逐一尝试 Directives 各项，包含外层 Note、内层 Tip。确认自定义标题只显示一次、Dropdown 默认收起、Initially open 默认展开。取消未应用草稿、撤销一次插入，并重启验证保存；导出 Book 后再使用 Jupyter Book 检查这些示例。