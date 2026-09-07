# TensorBoard 应用

入口：现有 TensorBoard 标签页，或工具服务卡片/摘要的“服务地址”。来源：页面读取与刷新实测。

1. 确认目标服务；需核对读取目录时查[服务摘要](../workspace/tool-services/tensorboard.md)。
2. 在 Time Series / Scalars 中检查 run 列表、勾选项、`Filter runs`（正则）与标签筛选；区分“列表没有”和“未选中/被筛掉”。
3. 点击 `Last Updated` 刷新控件，核对更新时间确实变化，再判断最新可见数据。
4. 按目标 run、tag、step/epoch 读取指标；不把平滑曲线或某一训练 step 当作最终验证结果。

**完成判据**：已读取所选 run/tag 的当前可见指标；页面无相应数据时如实说明，不据此推断训练状态。
