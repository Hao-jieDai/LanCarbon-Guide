---
title: Publishing Readiness
label: lancarbon-phase5-readiness
---

## English

### Phase 5A checks

Open a Book and choose Publish. LanCarbon checks Git, GitHub CLI, GitHub authentication, the most recent managed Book build, the saved repository binding and GitHub Pages. Each result is shown as passed, warning or error.

Git and GitHub CLI must be available in PATH. LanCarbon uses the account already authenticated by GitHub CLI and does not store a GitHub password or access token in notes.json. If GitHub CLI is missing, use Open GitHub CLI Download. If it is installed but signed out, use Sign in with GitHub CLI, finish authentication in the visible terminal, then select Refresh Checks.

A successful Book build is recommended now and required before Phase 5C publishes the real website. It does not block repository setup because Phase 5B prepares the remote destination without uploading Book files.

## 中文

### Phase 5A 检查

打开一本 Book 并点击 Publish。LanCarbon 会检查 Git、GitHub CLI、GitHub 登录状态、最近一次受管理构建、已保存的仓库绑定以及 GitHub Pages，并将结果显示为通过、警告或错误。

Git 与 GitHub CLI 必须能够通过 PATH 找到。LanCarbon 使用 GitHub CLI 已登录的账户，不会把 GitHub 密码或访问令牌写入 notes.json。GitHub CLI 缺失时点击 Open GitHub CLI Download；已经安装但未登录时点击 Sign in with GitHub CLI，在可见终端中完成认证，再点击 Refresh Checks。

建议先完成一次 Book Build；Phase 5C 发布真实网站前必须存在成功构建。Phase 5B 只准备远端目标，不上传 Book 文件，因此构建缺失在当前阶段只显示警告。