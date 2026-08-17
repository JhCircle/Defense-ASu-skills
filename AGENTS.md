# Defense-Asu-skills 协作规范

## 项目说明

Defense-Asu-skills 是中文求职**反酥化**工作流插件，用于把过度包装的经历还原成可核验事实，并生成面试追问与诚实版简历。

它与 [ASu-skills](https://github.com/Hisn00w/ASu-skills) 对称：ASu 负责「动作 → 招聘语言」；Defense-Asu 负责「招聘语言 → 动作与证据」。

## 修改规则

- 修改前先检查当前分支、工作区状态和远程更新。
- 反酥化词典与评级规则放在 `references/`；审计报告模板放在 `assets/`。
- README 中的图片使用仓库内相对路径，图片资源放在 `assets/` 下。
- 不在 skill、模板或 README 中写入真实姓名、电话、邮箱、密码、验证码或招聘隐私。
- 修改后检查 Markdown 冲突标记、路径、JSON 格式和相关技能的可用性。
- 创建 PR 前必须阅读根目录 [`CONTRIBUTING.md`](CONTRIBUTING.md) 和 [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md)。

## 提交规范

提交信息遵循 [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)：

```text
<type>: <中文简短标题>
```

常用类型：`feat:`、`fix:`、`docs:`、`refactor:`、`chore:`、`test:`。

示例：

```text
docs: 新增反酥化词典与职级对照表
feat: 新增 /probe 面试追问技能
fix: 修正贡献审计中未合并 PR 的判定文案
```

## 提交与 PR 前检查

```bash
git diff --check
git status --short
```

涉及技能修改时，人工走一遍对应 skill 的默认输出；涉及 HTML 时至少打开一次浏览器预览。
