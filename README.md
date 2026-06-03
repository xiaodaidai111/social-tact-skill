# 人情世故.skill

一套中文人际沟通 Skill 和通用大模型提示词，帮你把话说得真诚、自然、有分寸。

它不是教人圆滑，也不是教人套路别人，而是面向真实生活、学习、职场、饭局、客户沟通、长辈往来等场景，提供可以直接复制发送的话术。

## 适合谁

- 不知道怎么夸人，怕太油。
- 想感谢别人，但不想显得空泛。
- 想道歉，但不知道怎么承担责任和补救。
- 想拒绝别人，又不想把关系弄僵。
- 想请人帮忙、催进度、送礼、饭局发言，但怕失分寸。
- 想给 ChatGPT、Claude、Gemini、DeepSeek、Kimi、通义、豆包等模型一套稳定中文沟通提示词。

## 已包含 Skill

| 中文技能 | 内部 Skill 名 | 用途 |
| --- | --- | --- |
| 人情世故.skill | `renqing-shigu` | 总入口，判断关系、场景、分寸并路由到具体话术 |
| 恭维话.skill | `gongwei-hua` | 真诚、具体、不过界地夸人 |
| 感谢话.skill | `ganxie-hua` | 感谢领导、老师、前辈、朋友、客户 |
| 道歉话.skill | `daoqian-hua` | 为迟到、失误、忘回、工作疏漏道歉 |
| 拒绝话.skill | `tuiju-hua` | 婉拒邀约、帮忙、借钱、加班、合作 |
| 求人办事.skill | `qiuren-banshi` | 请人帮忙、请教、引荐、转发、看材料 |
| 饭局场面话.skill | `fanju-changmianhua` | 饭局开场、敬酒、感谢、圆场、离席 |
| 送礼话术.skill | `songli-huashu` | 送老师、长辈、客户、朋友礼物时的表达 |
| 催进度不伤人.skill | `cuijindu-bushangren` | 催回复、催交付、催确认，不显得咄咄逼人 |
| 朋友圈评论.skill | `pengyou-quanquan` | 朋友圈、群聊、评论区的自然互动短句 |

## 安装到 Codex

```powershell
Copy-Item -Recurse .\skills\renqing-shigu $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\gongwei-hua $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\ganxie-hua $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\daoqian-hua $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\tuiju-hua $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\qiuren-banshi $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\fanju-changmianhua $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\songli-huashu $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\cuijindu-bushangren $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\pengyou-quanquan $env:USERPROFILE\.codex\skills\
```

重启 Codex 或重新加载 Skills 后使用。

## 通用大模型使用

不是 Codex 也可以用：

- `UNIVERSAL_PROMPTS.md`：复制系统提示词到任意大模型。
- `adapters/chatgpt.md`：ChatGPT 用法。
- `adapters/claude.md`：Claude 用法。
- `adapters/gemini-deepseek-kimi.md`：Gemini、DeepSeek、Kimi、通义、豆包通用用法。
- `adapters/cursor-claude-code.md`：Cursor、Claude Code、代码编辑器 Agent 用法。

## 示例

```text
Use $gongwei-hua 帮我写三句夸领导今天分享的发言，要求自然一点。
```

```text
Use $ganxie-hua 帮我感谢老师帮我改论文，语气真诚但别太夸张。
```

```text
Use $tuiju-hua 帮我婉拒朋友借钱，不想伤感情。
```

```text
Use $cuijindu-bushangren 帮我催合作方今天确认方案，语气客气但要推进。
```

## 输出风格

默认给：

- 稳妥版
- 自然版
- 更正式版或高级一点版
- 不建议这么说
- 分寸提醒

## 设计原则

- 真诚，不油腻。
- 具体，不空泛。
- 有边界，不冒犯。
- 看关系、看场景、看目的。
- 先给可复制文本，再给分寸提醒。
- 对领导、老师、客户、长辈更克制。
- 对朋友、同学、同事可以更自然。

## 目录结构

```text
skills/
  renqing-shigu/
  gongwei-hua/
  ganxie-hua/
  daoqian-hua/
  tuiju-hua/
  qiuren-banshi/
  fanju-changmianhua/
  songli-huashu/
  cuijindu-bushangren/
  pengyou-quanquan/
adapters/
UNIVERSAL_PROMPTS.md
```

## License

MIT

