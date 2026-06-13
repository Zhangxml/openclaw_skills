# OpenClaw Skills

这是一个面向 OpenClaw / OpenCode 的 skills 集合仓库。

仓库按目录收录不同能力的 skill。每个 skill 通常以 `SKILL.md` 作为主说明文件，按需补充元数据、参考资料和辅助脚本，方便快速浏览、挑选和维护。

当前仓库共收录 10 个 skill。

## 仓库结构

大多数目录遵循下面的组织方式：

```text
<skill-name>/
|- SKILL.md
|- _meta.json / metadata.json
|- README.md
|- references/
`- scripts/
```

- `SKILL.md`：skill 的主入口和使用说明。
- `_meta.json` / `metadata.json`：发布或登记所需的元数据。
- `README.md`：补充说明，通常只在少数 skill 中出现。
- `references/`：背景资料、最佳实践、扩展文档。
- `scripts/`：供 skill 配套使用的脚本。

## 技能清单

| 目录 | 作用 | 关键文件 |
| --- | --- | --- |
| [agent-browser](./agent-browser/) | 基于 Rust 的无头浏览器自动化 skill，适合页面导航、点击、输入和快照。 | [`SKILL.md`](./agent-browser/SKILL.md), [`_meta.json`](./agent-browser/_meta.json) |
| [browser-automation](./browser-automation/) | 面向 OpenClaw 浏览器工具的操作规范，重点覆盖多步骤页面流程、登录检查和标签页管理。 | [`SKILL.md`](./browser-automation/SKILL.md) |
| [file-manager](./file-manager/) | 文件批量整理 skill，覆盖分类、重命名、去重和目录同步。 | [`SKILL.md`](./file-manager/SKILL.md), [`scripts/`](./file-manager/scripts/), [`references/`](./file-manager/references/) |
| [github](./github/) | 使用 `gh` CLI 与 GitHub 交互，处理 issue、PR、CI 和 API 查询。 | [`SKILL.md`](./github/SKILL.md), [`_meta.json`](./github/_meta.json) |
| [multi-search-engine](./multi-search-engine/) | 多搜索引擎集成 skill，支持国内外搜索引擎、时间过滤、站内搜索和知识查询。 | [`SKILL.md`](./multi-search-engine/SKILL.md), [`config.json`](./multi-search-engine/config.json), [`references/`](./multi-search-engine/references/) |
| [proactive-agent-lite](./proactive-agent-lite/) | 轻量级主动式 agent skill，聚焦记忆架构、反向提问和自修复模式。 | [`SKILL.md`](./proactive-agent-lite/SKILL.md), [`README.md`](./proactive-agent-lite/README.md), [`_meta.json`](./proactive-agent-lite/_meta.json) |
| [skill-vetter](./skill-vetter/) | 安装第三方 skill 前的安全审查 skill，用于排查权限范围和可疑模式。 | [`SKILL.md`](./skill-vetter/SKILL.md), [`_meta.json`](./skill-vetter/_meta.json) |
| [summarize](./summarize/) | 对 URL、本地文件、PDF、图片、音频和 YouTube 内容做摘要。 | [`SKILL.md`](./summarize/SKILL.md), [`_meta.json`](./summarize/_meta.json) |
| [tavily-search](./tavily-search/) | 基于 Tavily 的 Web 搜索 skill，返回相关结果、摘要片段和元数据。 | [`SKILL.md`](./tavily-search/SKILL.md), [`scripts/`](./tavily-search/scripts/), [`_meta.json`](./tavily-search/_meta.json) |
| [xiucheng-self-improving-agent](./xiucheng-self-improving-agent/) | 自我改进型 agent skill，用于分析对话质量并持续优化响应策略。 | [`SKILL.md`](./xiucheng-self-improving-agent/SKILL.md), [`self_improving.py`](./xiucheng-self-improving-agent/self_improving.py), [`skill.yaml`](./xiucheng-self-improving-agent/skill.yaml) |

## 如何使用

1. 先根据任务类型查看上面的技能清单，定位最接近的目录。
2. 优先阅读该目录下的 `SKILL.md`，确认 skill 的触发条件和使用边界。
3. 如果目录中存在 `README.md`、`references/` 或 `scripts/`，再继续查看补充资料和配套脚本。
4. 如果你在维护发布版本，再检查对应的 `_meta.json` 或 `metadata.json`。

## 维护说明

- 新增 skill 时，建议保持“一目录一个 skill”的组织方式。
- `SKILL.md` 应始终作为该 skill 的主入口。
- 如果 skill 依赖脚本或参考资料，优先放在同目录下的 `scripts/`、`references/` 中。
- 新增、删除或重命名 skill 后，请同步更新本 README 的技能清单。
