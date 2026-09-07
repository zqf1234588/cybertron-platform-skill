---
name: cybertron-platform
description: 操作 Cybertron 平台的文件管理、在线开发、SFTP/TensorBoard 工具服务和 PyTorch 训练任务；按目标直达页面，核对资源并查看 worker 日志和训练指标。
---

# Cybertron 平台

## 使用方式

1. 根据下表直接读取目标文档；已在目标页就从当前步骤继续，不返回首页重走。
2. 仅在文档给出的条件成立时读取辅助节点；达到完成判据即停止扩展检查。
3. 浏览器和标签页使用本次实际连接信息；复用已打开页面及已填表单，不固化 tab ID、任务 ID 或服务地址。

| 目标 | 直接读取 |
| --- | --- |
| 提交 PyTorch 训练 | [创建任务](references/training/templates/pytorch/create.md) |
| 找任务、核对提交状态 | [任务列表](references/training/tasks/index.md) |
| 看任务配置、生命周期 | [摘要](references/training/tasks/summary.md) |
| 看 CPU / GPU / 内存使用率 | [监控](references/training/tasks/monitor.md) |
| 看 epoch、metric、报错或下载日志 | [日志](references/training/tasks/logs.md) |
| 查项目目录与文件 | [文件管理](references/workspace/files.md) |
| 启动、打开开发环境或保存镜像 | [在线开发](references/workspace/online-development/index.md) |
| 新建开发环境 | [创建环境](references/workspace/online-development/create.md) |
| 找工具服务、查看服务入口 | [工具服务](references/workspace/tool-services/index.md) |
| 创建 SFTP / TensorBoard | [创建服务](references/workspace/tool-services/create.md) |
| 打开 TensorBoard、筛选或刷新曲线 | [TensorBoard 应用](references/apps/tensorboard.md) |

## 全局约束

- **项目**：使用本次任务指定的目标项目，核对完整名称；不在 skill 中保存真实项目名称或标识。
- **名称**：训练任务、在线开发环境用 `t` + 创建时系统时间 `yyMMddHHmm`；PowerShell：`Get-Date -Format "'t'yyMMddHHmm"`。同名时先核对是否已提交。
- **资源**：读取当前账户总额度与实际空闲量，区分 GPU 显存和主存；不预设特定账户配额。
- **创建/启动前**：合计训练、在线开发、推理、工具服务及已提交待启动的资源申请，按申请量而非利用率计算，按平台要求预留余量。核对 GPU、主存余量；占用不明先查清，不自行停止其他任务。
- 教学或查看请求不触发创建、启停、改文件。实际操作沿用当前用户授权，不重复征求已获得的许可。结果不明先查目标状态，避免重复提交。

## 结构约定

目录按界面归属组织，外部应用另放 `apps/`。只记录平台通用操作与不含身份信息的约定；具体项目路径、启动命令、实验协议与个案排查不收入本 skill，由当次任务提供。
**强连接**是文档中注明控件的直接、有向跳转；**辅助（弱连接）**是带触发条件的资料依赖，不表示页面有直达按钮。父子目录仅表示归属，不自动等于可点击跳转。
仅探索界面或维护结构时读取[导航图](references/navigation.md)。未教学节点保留位置、操作留空；用户教学、实测与推断分别标注，历史状态不作为实时结论。

发布约束：不写入真实账户、密码、令牌、个人联系信息、项目名称/ID/路径、私有镜像地址或账户配额；使用通用字段说明。备份、debug 记录和项目笔记不纳入发布内容。
