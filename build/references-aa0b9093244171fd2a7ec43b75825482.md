---
title: Cross References
label: phase-2-references
---

## English

### 1. Cross References

Give a heading a label by placing (label)= immediately before it. In this Book, labels should be unique. Links with an empty title automatically use the target title. Page Properties → Label names an entire page. Stable Export Paths let you link to a file even after renaming its title.

(guide-reference-target)=
#### A local reference target

- Local heading: [](#guide-reference-target).
- Equation on another page: [](#guide-carbon-balance).
- Another guide page: [](#phase-2-mathematics).
- Explicit link text: [Read the formula](#guide-carbon-balance).

The ref, eq and numref roles are also accepted. For example, {eq}`guide-carbon-balance` references the equation. Relative Markdown file links such as ../chapter/page.md#label are resolved against the current page's Export Path, inside this Book only. Hidden TOC pages remain referenceable. Clicking an internal reference selects its page and scrolls to the target, keeping Preview mode.

Missing or ambiguous references are marked and listed under Preview notices; they do not silently jump to an arbitrary page. Ordinary Notes resolve their own targets only. External links cannot navigate the Electron window. Equation numbering here is local to each page; verify final publication with Jupyter Book.

## 中文

### 1. Cross References / 中文

在标题前单独写一行 (label)= 即可给标题命名，同一本 Book 内应使用唯一 label。链接标题留空时会自动显示目标标题。Page Properties 中的 Label 命名整个页面；稳定的 Export Path 让标题重命名后文件链接仍然有效。

上面的四个链接依次演示：本页标题、另一页公式、另一篇教程页面，以及自定义链接文字。点击后应定位对应页面和目标，并保持 Preview 模式。

也支持 ref、eq、numref role，上面的 eq 示例引用另一页的碳收支公式。相对 Markdown 路径链接（例如 ../chapter/page.md#label）以当前页面的 Export Path 为基准，只在当前 Book 中解析。设置为不显示在目录中的页面仍可引用。

缺失或有歧义的引用会在正文中标记，并列入 Preview notices，不会随意跳到某个页面。普通 Notes 只解析自身目标。外部链接不能把 Electron 窗口导航到其他网站。当前公式按每页编号，正式发布编号请用 Jupyter Book 验证。

(acceptance-reference-page)=
## Reference Lab / 引用实验室

(acceptance-local-target)=
## Local target / 本页目标

English: each internal link below must reach the intended page or target.

中文：逐个点击以下链接，应定位正确的页面或目标。

1. Local heading / 本页标题：[](#acceptance-local-target)。
2. Explicit text / 指定文字：[返回本页目标](#acceptance-local-target)。
3. Cross-page heading / 跨页标题：[](#acceptance-typography)。
4. Relative file / 相对文件：[语法实验室](../../syntax-lab.md)。
5. File and fragment / 文件加锚点：[公式位置](../../syntax-lab.md#acceptance-balance)。
6. Whole-page label / 整页标签：[](#acceptance-syntax-page)。
7. Equation role / 公式角色：{eq}`acceptance-balance`。
8. Reference role / 引用角色：{ref}`acceptance-typography`。
9. Custom ref role / 自定义引用文字：{ref}`Typography / 文本样式 <acceptance-typography>`。
10. Numbered equation reference / 编号引用：{numref}`Equation %s <acceptance-balance>`。
11. Styled link / 带格式链接：[**加粗链接**及*斜体链接*](#acceptance-typography)。
12. Return home / 返回首页：[验收首页](../../index.md)。

## Acceptance record / 验收记录

| Check / 检查项 | Expected / 预期 |
| --- | --- |
| Edit → Preview → Edit | Original source preserved / 原文不变 |
| Internal reference click | Correct page and target / 正确页面与位置 |
| Preview → another page | Preview remains selected / 保持预览模式 |
| Dark / Light | Readable text and formulas / 文字公式可读 |
| Save → restart | Source and Book restored / 内容目录恢复 |
| Strict HTML build | Exit code 0 / 退出码为 0 |
| Jupyter Book start | Local website accessible / 网站可访问 |