# Defense-Asu-skills

<div align="center">
  <h3>中文求职反酥化工作流插件</h3>
  <p>把招聘语言还原成可核验动作。酥化过 HR 筛选；反酥化过面试第二个问题。</p>
</div>

对称于 [ASu-skills](https://github.com/Hisn00w/ASu-skills)：ASu 把真实经历写成招聘语言；Defense-Asu 把招聘语言拆回事实、证据与追问。

| 入口 | 用途 | 主要交付 |
| ---- | ---- | -------- |
| `/deasu` | 经历反酥化 | 强主张审计表、可守住版表述、证据缺口 |
| `/audit-contrib` | 开源贡献审计 | 贡献水分卡、PR/diff 对照、降级写法 |
| `/resume-audit` | 简历打标 | 水分等级、红旗清单、修改优先级 |
| `/honest-resume` | 诚实版简历 | 去包装可编辑 HTML + 删改摘要 |
| `/probe` | 面试追问 | 「第二个问题」脚本、期望证据、不合格信号 |

## 安装

把仓库发给 Codex / Claude Code，并说明要安装插件：

```text
请从这个 GitHub 仓库安装 Defense-Asu-skills 插件，并启用 deasu、audit-contrib、resume-audit、honest-resume、probe：
https://github.com/JhCircle/Defense-Asu-skills
```

安装后新建对话，输入 `/` 选择对应 skill；或使用：

```text
$deasu 请反酥化下面这段简历要点，标出红黄绿并给出可守住版。
$audit-contrib 对照这些 PR 链接，审计我简历里的开源贡献写法。
$resume-audit 给我的简历打水分等级和红旗清单。
$honest-resume 根据审计结果生成诚实版可编辑 HTML 简历。
$probe 按技术一面标准，对我的项目经历生成追问脚本。
```

## `/deasu`：经历反酥化

适合：

- 把「主导 / 0→1 / 治理专项」还原成实际动作；
- 审计 ASu `/asu` 输出是否过冲；
- 面试前自查：哪些句子答不上第二个问题。

```text
/deasu

目标岗位：AI 应用工程师
下面是酥化后的简历要点，请还原事实边界并给出可守住版。
```

## `/audit-contrib`：开源贡献审计

专门处理「错别字 → Main Contributor」换算。对照 PR、diff、合并状态，输出水分卡。

硬规则：**没 merge 就不能写被项目采用。**

```text
/audit-contrib

简历开源段落：…
PR 列表：…
```

## `/resume-audit`：简历打标

整份扫描强动词、数字口径、头衔膨胀与工具堆砌，给出水分等级与修改优先级。

## `/honest-resume`：诚实版简历

基于反酥化结论生成单栏可编辑 HTML（模板：`assets/honest-resume-template.html`）。先站得住，再谈好看。

## `/probe`：面试追问

为每条高风险主张生成主问 + 追问、期望证据与不合格回答信号。求职者可自测，也可用于互助面。

## 五个入口如何配合

1. `/resume-audit` 或 `/deasu` 找出过冲主张；
2. 开源段落用 `/audit-contrib` 对照 diff；
3. `/probe` 模拟第二个问题，确认删改；
4. `/honest-resume` 输出可投递的诚实版文件。

也可与 ASu-skills 串联：先 `/asu` 写进取版，再 `/deasu` 压回可守住版。

## 事实边界

- 证据不足标「待核实」，不直接定罪；
- 区分包装过猛与欺诈：前者降级，后者建议删除；
- 不教用户圆谎；
- 不在公开文件中写入真实电话、邮箱、密码、验证码或招聘隐私。

## 文件结构

```text
Defense-Asu-skills/
├── .codex-plugin/plugin.json
├── skills/
│   ├── deasu/
│   ├── audit-contrib/
│   ├── resume-audit/
│   ├── honest-resume/
│   └── probe/
├── assets/
│   ├── claim-audit-report.html
│   └── honest-resume-template.html
├── references/
│   └── deasu-dictionary.md
├── CONTRIBUTING.md
└── README.md
```

## 与 ASu-skills 对照

| ASu | Defense-Asu |
| --- | -------- |
| `/contributor` | `/audit-contrib` |
| `/asu` | `/deasu` |
| `/resume` | `/resume-audit` |
| `/asu-resume` | `/honest-resume` |
| `/offer` | `/probe`（面试侧，而非投递漏斗） |

词典与换算表见 [references/deasu-dictionary.md](references/deasu-dictionary.md)，灵感来自 ASu 贡献指南中的「反酥化」一节。

## 开源协议

[MIT License](LICENSE)
