# 人情世故.skill

一个 Codex Skill 项目，用来生成更得体、更自然、更有分寸的中文人际沟通表达。

它不是教人圆滑，也不是教人套路别人，而是帮助你在真实场景里把话说得：

- 真诚
- 具体
- 不冒犯
- 不油腻
- 不越界
- 能直接复制发送

## 已包含技能

### 1. 恭维话.skill

内部 Skill 名：`gongwei-hua`

用途：生成真诚、具体、不过界的中文夸奖话术。

适用场景：

- 夸领导发言
- 夸老师讲得清楚
- 夸同事做事靠谱
- 夸客户反馈专业
- 夸朋友有想法
- 写朋友圈/群聊/评论区的得体赞美

示例：

```text
Use $gongwei-hua 帮我写三句夸领导今天分享的发言，要求自然一点。
```

```text
Use $gongwei-hua 帮我夸一下老师今天讲的案例，别太油。
```

## 总入口

### 人情世故.skill

内部 Skill 名：`renqing-shigu`

用途：处理更宽泛的人际沟通、场面话、客套话、感谢、道歉、拒绝、求人办事、饭局话术等。

示例：

```text
Use $renqing-shigu 帮我组织一段饭局上感谢前辈照顾的话。
```

## 后续可扩充技能

我建议按下面顺序扩充：

1. `ganxie-hua`：感谢话.skill  
   用于感谢老师、领导、前辈、朋友、客户，不空泛、不卑微。

2. `daoqian-hua`：道歉话.skill  
   用于迟到、失误、忘回消息、工作疏漏，重点是承担责任和补救。

3. `tuiju-hua`：拒绝话.skill  
   用于婉拒邀约、请求、加班、借钱、帮忙，既留余地又不含糊。

4. `qiuren-banshi`：求人办事.skill  
   用于请人帮忙、请教、引荐、催回复，强调低压力、给台阶、讲清楚成本。

5. `fanju-changmianhua`：饭局场面话.skill  
   用于敬酒、开场、感谢、圆场、离席、介绍人，注意不尴尬不过火。

6. `songli-huashu`：送礼话术.skill  
   用于送老师、长辈、客户、朋友礼物时的简短表达，避免功利感。

7. `cuijindu-bushangren`：催进度不伤人.skill  
   用于催同学、同事、合作方、客户回复或交付，不显得咄咄逼人。

8. `pengyou-quanquan`：朋友圈评论.skill  
   用于朋友圈、群聊、评论区的短句互动，轻松自然不尬聊。

## Install

### Codex Skill

```powershell
Copy-Item -Recurse .\skills\renqing-shigu $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\gongwei-hua $env:USERPROFILE\.codex\skills\
```

Restart Codex or reload skills after installing.

### 通用大模型

如果不是 Codex，也可以直接使用：

- `UNIVERSAL_PROMPTS.md`：复制里面的系统提示词到任意大模型。
- `adapters/chatgpt.md`：ChatGPT 用法。
- `adapters/claude.md`：Claude 用法。
- `adapters/gemini-deepseek-kimi.md`：Gemini、DeepSeek、Kimi、通义、豆包等通用用法。
- `adapters/cursor-claude-code.md`：Cursor、Claude Code、代码编辑器 Agent 用法。

## Design Principles

- 真诚，不油腻。
- 具体，不空泛。
- 有边界，不冒犯。
- 看关系、看场景、看目的。
- 先给可复制文本，再给分寸提醒。
- 对领导、老师、客户、长辈要更克制。
- 对朋友、同学、同事可以更自然。

## Repository Layout

```text
skills/
  renqing-shigu/
    SKILL.md
    agents/openai.yaml
  gongwei-hua/
    SKILL.md
    agents/openai.yaml
    references/
      compliment-patterns.md
      compliment-checklist.md
adapters/
  chatgpt.md
  claude.md
  gemini-deepseek-kimi.md
  cursor-claude-code.md
UNIVERSAL_PROMPTS.md
```
