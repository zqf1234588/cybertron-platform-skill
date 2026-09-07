# 导航图（按需读取）

平台入口：使用本次任务提供的 Cybertron 门户地址，进入工作空间。主页与工作空间、训练等是侧栏同级项；面包屑中的“主页”不代表它们属于主页页面。

## 界面归属

```text
平台侧栏
├─ 主页〔留空〕
├─ 工作空间
│  ├─ 文件管理 → 目录树 / 当前目录
│  ├─ 在线开发 → 创建环境 / 具体环境
│  │  └─ 具体环境 → 打开开发应用 / 更多（保存、另存为）
│  └─ 工具服务 → 创建服务 / 具体服务
│     ├─ SFTP → 摘要 / 日志〔留空〕
│     └─ TensorBoard → 摘要 / 日志〔留空〕
├─ 训练
│  ├─ 任务模板 → PyTorch → 创建任务
│  └─ 任务管理 → 具体任务 → 摘要 / 监控 / 日志 / 终端
├─ 推理〔留空〕
├─ 项目〔留空〕
├─ 镜像〔留空〕
├─ 模型〔留空〕
├─ 数据〔留空〕
└─ 计费〔留空〕

外部应用：Jupyter〔内部操作留空〕、TensorBoard
```

## 节点索引

| 归属 | 节点文档 |
| --- | --- |
| 工作空间 | [文件管理](workspace/files.md)；[在线开发](workspace/online-development/index.md)、[创建环境](workspace/online-development/create.md) |
| 工作空间 → 工具服务 | [列表](workspace/tool-services/index.md)、[创建](workspace/tool-services/create.md)、[SFTP](workspace/tool-services/sftp.md)、[TensorBoard](workspace/tool-services/tensorboard.md) |
| 训练 → 任务模板 → PyTorch | [创建任务](training/templates/pytorch/create.md) |
| 训练 → 任务管理 | [列表](training/tasks/index.md)、[摘要](training/tasks/summary.md)、[监控](training/tasks/monitor.md)、[日志](training/tasks/logs.md)、[终端](training/tasks/terminal.md) |
| 外部应用 | [TensorBoard](apps/tensorboard.md) |

## 关系维护

- 节点的“跳转”记录 `控件 → 目标`：有向强连接，注明运行状态等前提；双向关系须分别有依据。
- 节点的“辅助”记录 `问题/条件 → 所需资料`：弱连接，仅条件成立时读取。
- 入口目标表直接链接操作节点，避免逐层读索引。关系只在源节点维护，不再复制一份 JSON 图。
- 仅收录平台通用知识与不含身份信息的约定，不新增具体项目或个案问题节点。新知识补入所属节点；仅当内容能独立完成一个目标且需要按需加载时拆文件。不为每个按钮建文件。
- 尚未教学的流程保持留空；新增直达路径须有实际可见链接或用户教学依据，不推测路由。
