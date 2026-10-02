# DSH 写路径验证

这个文件由 GitHub 接入的端到端写验证创建，用来证明三条写路径都真实可用：

- `create_branch` —— 建分支
- `create_or_update_file` —— 经 Contents API 提交文件
- `create_pull_request` —— 开 PR

三次调用都经过 DSH 的**原生审批弹窗**（`tools/pre-execute` → `kind:'ask'`）逐次授权，
不是静默执行。

验证时间：2026-10-02
分支：dsh-verify-20261002
本文件可以安全删除。
