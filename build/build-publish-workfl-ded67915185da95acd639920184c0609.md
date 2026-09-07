---
title: Build and Publishing Workflow
label: lancarbon-phase5-build-publish-workflow
---

## English

### Three independent outputs

LanCarbon stores the authoritative Book in its own data location. Build reads the latest saved Book directly; it does not read a manually exported folder. Export remains a separate way to create a source copy for backup or external editing, and its destination must be empty. Export is not required before Build or Publish.

### First build and later rebuilds

The first build uses Choose Location and Build and remembers a managed destination for this Book. Later, Rebuild Website reuses that location without opening a folder picker. Change Build Location is available when the managed website should move elsewhere. LanCarbon builds in a temporary folder and replaces the previous managed website only after success.

The Build panel compares the current Book with the source fingerprint saved by the last successful build. Build is up to date means the managed website matches the current pages, hierarchy and settings. Book changed — rebuild required means the Book was edited afterward. This state survives restarting LanCarbon.

### One-step online updates

Publish Website is used when the managed build is current. If the Book is new or changed, the action becomes Build and Publish Website or Rebuild and Update Website. LanCarbon saves the Book, validates it, rebuilds the managed website at its remembered location, creates the repository-specific Pages build, uploads it and verifies the deployed commit. Only a first build or a missing build location asks for a folder.

A failed rebuild keeps the previous local website and stops before publishing. A network or GitHub failure keeps the previous online website. Open Pages and Open Repository remain available for inspection.

## 中文

### 三种相互独立的输出

LanCarbon 自己的数据位置保存权威版本的 Book。Build 会直接读取软件中最新保存的 Book，不读取手动 Export 的文件夹。Export 继续用于生成备份或供外部编辑的源文件副本，目标文件夹必须为空；Build 和 Publish 之前都不需要先 Export。

### 首次构建与后续重建

第一次构建使用 Choose Location and Build，并为当前 Book 记住受管理的构建位置。以后点击 Rebuild Website 会直接复用该位置，不再打开文件夹选择器。需要移动构建网站时使用 Change Build Location。LanCarbon 始终先在临时文件夹构建，成功后才替换上一次受管理网站。

Build 面板会比较当前 Book 与上次成功构建保存的内容指纹。Build is up to date 表示受管理网站与当前页面、层级和设置一致；Book changed — rebuild required 表示 Book 在构建后又被修改。重启 LanCarbon 后该状态仍然有效。

### 一步完成在线更新

:::{div}
:class: lc-align-center

一步更新
:::

受管理构建为最新时使用 Publish Website。如果 Book 尚未构建或构建已经过期，按钮会变成 Build and Publish Website 或 Rebuild and Update Website。LanCarbon 会依次保存、检查、在已记住的位置重建、生成适合当前仓库地址的 Pages 版本、上传并核实实际部署提交。只有首次构建或原构建位置丢失时才需要选择文件夹。

重建失败时保留上一次本地网站，并停止发布；网络或 GitHub 失败时保留上一次线上网站。Open Pages 与 Open Repository 可随时用于检查。