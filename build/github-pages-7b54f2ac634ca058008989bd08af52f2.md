---
title: GitHub and Pages Setup
label: lancarbon-phase5-github-pages
---


### Connect an existing repository

Choose Publish, select Existing repository, and enter the owner, repository name and publication branch. The default branch is gh-pages. Your authenticated account needs repository administration access. Connect and Initialize Pages verifies the repository, creates the publication branch from its default branch when necessary, and configures GitHub Pages to serve the branch root. Existing files and branches are retained.

### Create a repository

Select New repository, choose Public or Private, and enter the owner and repository name. Create Repository and Pages creates the repository with an initial README, prepares the publication branch, enables Pages and saves the binding only for this Book. Private repository Pages availability depends on the GitHub account and organization plan.

The connected repository URL is also written to Book settings and exported metadata. Open Repository and Open Pages use HTTPS. Reconfiguring a Book does not delete the old repository. If setup partly succeeds and Pages configuration fails, LanCarbon reports the repository URL so it can be inspected or reconnected; it never deletes the remote repository automatically.

Phase 5A and 5B stop after environment checks, repository binding and Pages initialization. Publishing or updating the generated Book website belongs to Phase 5C.



### 连接已有仓库

点击 Publish，选择 Existing repository，填写 owner、仓库名和发布分支；默认分支为 gh-pages。当前登录账户需要具有仓库管理权限。Connect and Initialize Pages 会核对仓库，必要时从默认分支创建发布分支，并配置 GitHub Pages 从该分支根目录提供网站；原有文件和分支不会被删除。

### 创建新仓库

选择 New repository，设置 Public 或 Private，并填写 owner 与仓库名。Create Repository and Pages 会创建带初始 README 的仓库、准备发布分支、启用 Pages，并仅为当前 Book 保存绑定。私有仓库能否使用 Pages 取决于 GitHub 账户或组织套餐。

连接后的仓库网址也会写入 Book settings 和导出元数据。Open Repository 与 Open Pages 使用 HTTPS。更改绑定不会删除旧仓库。如果仓库已经创建、但 Pages 配置失败，LanCarbon 会显示仓库网址供检查或重新连接，不会自动删除远端仓库。

Phase 5A 与 5B 到环境检查、仓库绑定和 Pages 初始化为止；上传或更新实际 Book 网站属于 Phase 5C。