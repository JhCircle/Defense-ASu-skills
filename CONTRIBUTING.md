# 贡献指南

本仓库对贡献一律**反酥化**处理：写清楚你改了什么，不要写成治理专项。

## 反酥化对照（投稿时用）

| 你想写的 | 本仓库认可的写法 |
| -------- | ---------------- |
| 主导反酥化体系建设 | 给词典加了一行映射 |
| 负责插件架构升级 | 改了 `plugin.json` 的描述字段 |
| 深度参与 agent 对齐 | 修了 `SKILL.md` 里的错别字 |

头衔无效。diff 有效。

## 怎么贡献

1. Fork 后从 `main` 拉分支，例如 `docs/fix-dictionary`；
2. 一个 PR 只做一件事；
3. 改 skill 就按该 skill 默认输出走查一遍；改 HTML 就在浏览器打开，确认可编辑、可打印；
4. commit 使用 Conventional Commits + 中文标题，例如 `docs: 补充数字口径追问示例`；
5. 创建 PR 前阅读本文件和 [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md)。

## 我们欢迎的贡献

- 反酥化词典的真实案例（匿名化）；
- 更准的风险判定规则与追问模板；
- 诚实版简历模板的排版与无障碍改进；
- 在 Codex / Claude Code / Cursor 下的加载与触发反馈。

## 不会合的贡献

- 教人更隐蔽地夸大经历、绕过追问；
- 删除「不教圆谎 / 证据不足标待核实」等边界条款；
- 无意义换行、标点反复横跳；
- 写入真实姓名、电话、邮箱、token 或未公开招聘信息。

## 与 ASu-skills 的关系

本项目是 [ASu-skills](https://github.com/Hisn00w/ASu-skills) 的对称插件，不是它的 fork 敌对。可以同时安装：一边酥化进取版，一边反酥化压回可守住版。
