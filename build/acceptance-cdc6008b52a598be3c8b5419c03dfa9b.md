---
title: Phase 4 Acceptance
label: lancarbon-phase4-acceptance
---


### Phase 4D checklist

1. Open an existing Book and run Build. Confirm preflight reports page, reference, citation and resource problems before the CLI starts.
2. Correct every blocking error. Confirm warnings can remain and a successful strict build reports 0 errors unless the CLI reports a real failure.
3. Confirm the managed folder contains .lancarbon-build.json and _build/html/index.html. Open several pages, images, downloads, cross-references and citations in the local website.
4. Use Stop Website, then Start Website. Confirm stopping does not delete files and the restored address serves the same website.
5. Restart LanCarbon, reopen Build and start the saved website without rebuilding. An unrelated local server, including port 3000, must remain available.
6. Make a disposable syntax error and rebuild. Confirm the new build fails, its real diagnostic remains visible, retry stays available, and the last successful files remain intact.
7. Remove the syntax error, rebuild, and confirm the website changes only after success. Expand Jupyter Book output when full CLI evidence is needed.

Phase 4 is accepted when the checks, safe build, saved output and local website lifecycle all pass. Publishing to a remote host and executable notebooks remain later work.



### Phase 4D 验收清单

1. 打开已有 Book 并运行 Build，确认 CLI 启动前会检查页面、引用、文献和资源问题，并尽量显示页面与行号。
2. 修正全部阻断错误；警告可以保留。严格构建成功时应显示 0 errors，除非 CLI 确实报告失败。
3. 确认受管理目录包含 .lancarbon-build.json 和 _build/html/index.html；在本地网站中检查多个页面、图片、附件下载、交叉引用和文献引用。
4. 依次使用 Stop Website 和 Start Website，确认停止服务不会删除文件，恢复后的地址仍提供同一网站。
5. 重启 LanCarbon，重新打开 Build，不重新构建即可启动已保存网站；其他本地服务（包括 3000 端口）应继续可用。
6. 在可丢弃内容中制造语法错误并重新构建，确认新构建失败、真实诊断可见、可以立即重试，并保留上一次成功文件。
7. 删除语法错误并重新构建，确认只有成功后网站才更新；需要完整 CLI 证据时展开 Jupyter Book output。

检查、可靠构建、长期保存结果及本地网站生命周期全部通过后，即完成 Phase 4 验收。远程发布和可执行 Notebook 仍属于后续工作。

