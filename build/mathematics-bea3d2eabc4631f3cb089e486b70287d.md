---
title: Tables and Mathematics
label: phase-2-mathematics
---


### 1. Mathematics and Equations

Inline mathematics uses single dollar signs: $E=mc^2$. The equivalent role is {math}`a^2+b^2=c^2`.

A labelled equation uses the math directive. Switch to Edit to see its exact source; Preview should show a typeset fraction and an equation number:

```{math}
:label: guide-carbon-balance
\Delta C = E - R, \qquad f = \frac{R}{E}
```

See [](#guide-carbon-balance). Dollar blocks also work:

$$
\sum_{i=1}^{n} C_i = C_{\mathrm{total}}
$$

KaTeX and its fonts are bundled: no internet is needed. Page YAML frontmatter can define a math mapping of macro names to strings. Invalid formulas show their source and a Preview notice; fix them in Edit. Unsafe HTML/URL macros are disabled. Local equation numbers may differ from custom numbering in the final website.

(table-math-panels)=
### 2. Tables and Math Panels

#### Tables

1. Put the cursor at the insertion point and click **Table**. To edit an existing regular Markdown table, put the cursor inside it first.
2. Set **Columns** and **Data rows (excluding header)**. The panel supports 1–20 columns and 1–100 data rows.
3. Fill the header and data cells. Tab/Shift+Tab moves between cells; each column has Default, Left, Center and Right alignment choices.
4. Click a cell before using Insert row below, Delete row, Insert column right or Delete column. The selected cell determines where the operation takes place. The header and last remaining data row/column cannot be deleted through these controls.
5. Click **Apply**, then Preview to inspect the table. Cancel leaves the original note unchanged. Merged cells, nested/irregular tables and list-table directives require source editing.

#### Math

Click **Math** and choose **Inline** or **Display**. Enter the formula itself, without surrounding dollar signs. Inline wraps the formula in single dollar signs; Display uses double dollar signs on separate lines. Multiline formulas need Display mode.

Templates include Fraction, Root, Superscript, Subscript, Scripts, Sum, Integral, Brackets, Aligned equations, Greek letters and operators. The editable placeholder is selected after insertion. For matrices, set Matrix rows and Matrix columns (1–10) and click Insert matrix.

The preview renders offline as you type. Correct invalid formulas before applying. A regular existing formula can be reopened; labelled equations, macros and advanced MyST math directives should be edited in source so their extra information is retained.

#### Try it

Create a two-column table, right-align the numeric column, apply it and reopen it to change a cell. Undo and redo that edit. Insert a Fraction template, replace its selected placeholder, and inspect the preview. Cancel a second draft and confirm the saved note is unchanged.



### 1. Mathematics and Equations / 中文

行内公式使用单个美元符号，例如上面的能量公式；等价写法是 math role。点击 Edit 可以查看美元符号和 role 的完整源码，Preview 中应显示排版后的公式，而不是源码标记。

上面的 math directive 定义了碳收支公式，其中 label 为 guide-carbon-balance。预览应显示分式和公式编号；点击“See”后面的引用应跳到该公式。双美元符号包围的公式块也可以正常排版，上方总和公式就是例子。

KaTeX 及其字体随软件安装，不需要网络。页面 YAML frontmatter 中的 math 映射可以定义字符串宏。无效公式会保留源码并出现在 Preview notices 中，请返回 Edit 修正。出于安全考虑，HTML/URL 宏被禁用。本地公式编号可能与最终网站的自定义编号不同。

### 2. Tables and Math Panels / 中文

#### 表格

1. 把光标放在插入位置，点击 **Table**。编辑已有规则 Markdown 表格时，先把光标放进表格内部。
2. 设置 **Columns** 和 **Data rows (excluding header)**，支持 1–20 列、1–100 行数据，表头单独计算。
3. 填写表头和单元格，用 Tab/Shift+Tab 切换；每列可选默认、左、中、右对齐。
4. 先点击目标单元格，再使用下方插入行、删除行、右侧插入列、删除列。操作位置由选中单元格决定；表头及最后一行数据、最后一列不能通过这些按钮删除。
5. 点击 **Apply**，切换 Preview 检查结果；Cancel 不改变原文。合并单元格、嵌套或不规则表格、list-table 指令需要源码编辑。

#### 公式

点击 **Math**，选择 **Inline**（行内）或 **Display**（独立）。只填写公式，不填写外层美元符号；应用后自动生成行内或独立公式语法。多行公式需要使用 Display。

模板包含分数、根号、上下标、组合上下标、求和、积分、括号、多行对齐、希腊字母和运算符；插入后会选中待替换位置。矩阵可设置 1–10 行和列，再点击 Insert matrix。

预览随输入离线更新。公式无效时先修正再应用。普通已有公式可以再次打开；带标签、宏及复杂 MyST 指令的公式继续通过源码编辑，保留原有信息。

#### 练习

创建两列表格，将数字列右对齐，应用后重新打开并修改单元格，再撤销和重做。插入 Fraction 模板并替换选中部分，观察公式预览。取消第二份草稿，确认已保存正文不变。