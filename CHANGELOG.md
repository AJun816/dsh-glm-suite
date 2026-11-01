# Changelog

All notable changes to this project are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/); versions follow semver.

> 0.3.0 起从 dsh-model-failover 仓库（v0.9.x 的 packages/glm-suite）拆分为独立仓库；历史变更见彼处 CHANGELOG。

## [0.3.0] — 2026-11-01

### Changed — 独立仓库起步
- 从 dsh-model-failover 一仓双插件形态拆分为独立仓库（包在仓库根，安装源即本仓库）。
- 仓库元数据（repository/keywords/homepage）、CI（node 22/24 单测）、LICENSE(MIT)、CHANGELOG 就位。

### 继承自 0.2.x（拆分前最后状态）
- 四 MCP 封装：web_search_prime（provider zhipu-official）/ webReader（provider zhipu-reader，本地 http 兜底）/ zread 三工具 / glm_vision_* 八件（本地 stdio 桥，懒启动）。
- 多 key 池轮换：1310/1308 等窗口错误解析重置时刻冷却换号；1113/1309/1313/1000-1003 永久标记；搜索池耗尽显式失败，绝不回落 DeepSeek 计费。
- 0.2.1 修复：配置端点字段接入客户端（URL 变更重建）；二进制内容兜底显式 unsupported；死代码清理。
- 测试：9 单测 + apply 级 10 断言集成 + 真 key 冒烟（1310 轮换/reader/zread/12s 识图）。
