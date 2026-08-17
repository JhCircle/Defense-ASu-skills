---
name: audit-contrib
description: 开源贡献反酥化审计技能：对照 PR、diff、合并状态检验简历中的开源贡献写法，识别 typo-only 膨胀与未合并冒充已采用；当用户输入“/audit-contrib”“审计开源贡献”或要求核对 contribution graph 时使用。
---

# /audit-contrib：开源贡献审计

专门拆穿「一个错字 = 文档质量治理专项」这类换算。PR 本体可以很小；问题出在写进简历之后的叙事。

## 与 /contributor 的关系

| ASu `/contributor` | Defense-Asu `/audit-contrib` |
| ------------------ | ------------------------- |
| 找 typo / README 小修并提 PR | 读 PR/diff，判断简历叙事是否过冲 |
| 合并后交给 `/asu` 酥化 | 合并前后都可审计，未合并不得写「被采用」 |
| 贡献证据卡 | 贡献水分卡 |

## 工作流程

1. 收集材料：简历中的开源段落、PR 链接、仓库名、GitHub 用户名、贡献说明。
2. 对每个声称的贡献只读拉取或根据用户提供的 diff/截图确认：改动文件、行数、类型（typo / docs / test / bugfix / feature）、是否合并、CI/review 情况。
3. 分类标签（可多选）：
   - `typo-only` / `docs-only` / `link-fix` / `formatting`
   - `test` / `bugfix` / `feature` / `infra`
   - `merged` / `open` / `closed-unmerged` / `draft`
   - `drive-by`（与长期维护无关的一次性小改）
4. 对照简历原文，标出过冲点：把 typo 写成治理专项、把 open PR 写成被采用、把多仓库小修写成架构协作等。
5. 输出**贡献水分卡**与可守住写法；需要整体经历还原时转入 `/deasu`，需要追问脚本时转入 `/probe`。

## 判定规则

- 没 merge：最多写「已提交 / 协作中」，禁止「被项目采用」「落地」「上线」。
- typo / 标点 / 坏链接 / formatting：诚实写法允许「文档勘误」「修复失效链接」；禁止「主导文档质量治理」「覆盖率 100%」「Core Maintainer」。
- 多个同类小 PR：可以写「在 N 个仓库提交了文档/链接修复」并附链接；不要升级成「跨项目质量体系建设」。
- 仓库 `CONTRIBUTING` 明确禁止 typo-only 的贡献，若仍写入简历夸大价值，额外标 `红：规范规避风险`。
- 无链接又无 diff：整条标黄或红，要求补证据，不替用户圆谎。

## 默认输出

1. 贡献清单表：仓库 | PR | 状态 | 改动类型 | 简历原文 | 可守住写法 | 风险；
2. 总评：水分等级 + 最危险的 1—3 条；
3. 面试官可能问的 diff 级问题；
4. 给求职者的修改建议（删 / 降级 / 补链接）。

## 边界

- 只读审计默认不 fork、不 push、不代提 PR。
- 不公开辱骂维护者或贡献者；语气可以锋利，但结论必须可复核。
- 不把真实邮箱、token、私有仓库内容写进仓库文件。
