# Cursor / Claude Code / 代码编辑器 Agent 用法

这类工具可以直接读取本仓库的 Markdown 文件。建议让 Agent 先读：

```text
UNIVERSAL_PROMPTS.md
skills/gongwei-hua/SKILL.md
skills/gongwei-hua/references/compliment-patterns.md
skills/gongwei-hua/references/compliment-checklist.md
```

## 使用方式

```text
请读取本仓库的人情世故.skill 规则，然后帮我生成一段恭维话。

场景：
对象：
关系：
目的：
语气：
```

## 如果要扩充新技能

新增技能时建议保持：

```text
skills/
  skill-name/
    SKILL.md
    agents/openai.yaml
    references/
```

并在 `README.md` 的“后续可扩充技能”里登记。

