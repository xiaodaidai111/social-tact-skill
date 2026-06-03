# 人情世故.skill

一套中文人际沟通 Skill 和通用大模型提示词，专门处理夸人、感谢、道歉、拒绝、求人办事、饭局话、送礼、催进度、朋友圈评论、微信表情包等高频场景。

核心能力：

- 根据聊天上下文判断关系、场景、目的和风险。
- 分析对方性格与沟通偏好，对症下药。
- 根据真实聊天习惯控制长短、语气、停顿和信息量。
- 生成能直接复制发送的中文话术。
- 给出稳妥版、自然版、正式版和不建议说法。
- 适配 Codex、ChatGPT、Claude、Gemini、DeepSeek、Kimi、通义、豆包、Cursor、Claude Code 等模型。

## 适合谁

- 不知道怎么夸人，怕太油。
- 想感谢别人，但不想显得空泛。
- 想道歉，但不知道怎么承担责任和补救。
- 想拒绝别人，又不想把关系弄僵。
- 想请人帮忙、催进度、送礼、饭局发言，但怕失分寸。
- 想让大模型根据对方性格生成更贴合的回复。

## 已包含 Skill

| 中文技能 | 内部 Skill 名 | 用途 |
| --- | --- | --- |
| 人情世故.skill | `renqing-shigu` | 总入口，分析上下文、关系、性格和场景，路由到具体话术 |
| 恭维话.skill | `gongwei-hua` | 真诚、具体、不过界地夸人 |
| 感谢话.skill | `ganxie-hua` | 感谢领导、老师、前辈、朋友、客户 |
| 道歉话.skill | `daoqian-hua` | 为迟到、失误、忘回、工作疏漏道歉 |
| 拒绝话.skill | `tuiju-hua` | 婉拒邀约、帮忙、借钱、加班、合作 |
| 求人办事.skill | `qiuren-banshi` | 请人帮忙、请教、引荐、转发、看材料 |
| 饭局场面话.skill | `fanju-changmianhua` | 饭局开场、敬酒、感谢、圆场、离席 |
| 送礼话术.skill | `songli-huashu` | 送老师、长辈、客户、朋友礼物时的表达 |
| 催进度不伤人.skill | `cuijindu-bushangren` | 催回复、催交付、催确认，不显得咄咄逼人 |
| 朋友圈评论.skill | `pengyou-quanquan` | 朋友圈、群聊、评论区的自然互动短句 |
| 微信表情包指导.skill | `wechat-biaoqingbao` | 判断一句话里哪里插表情包、插哪类最合适 |

## 安装到 Codex

在项目根目录运行这一条：

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null; Copy-Item -Recurse -Force .\skills\* "$env:USERPROFILE\.codex\skills\"
```

重启 Codex 或重新加载 Skills 后使用。

## 国内大模型快速用法

国内大模型有时记不住很长的初始提示词，推荐每次提问都带上这个短模板：

```text
请按“人情世故.skill”处理：
先分析上下文、关系、对方性格、我的目的和风险，再给可直接发送的话。
输出：稳妥版、自然版、正式版、不建议说法、分寸提醒。

场景：
对方是谁：
对方性格：
聊天上下文：
我想达到的目的：
希望语气：
原话/草稿：
```

更完整的通用提示词见：`UNIVERSAL_PROMPTS.md`。

## 通用大模型使用

- `UNIVERSAL_PROMPTS.md`：复制到任意大模型使用。
- `adapters/chatgpt.md`：ChatGPT 用法。
- `adapters/claude.md`：Claude 用法。
- `adapters/gemini-deepseek-kimi.md`：Gemini、DeepSeek、Kimi、通义、豆包通用用法。
- `adapters/cursor-claude-code.md`：Cursor、Claude Code、代码编辑器 Agent 用法。

## 示例

更多真实聊天示例见：`examples/real-chat-examples.md`

```text
Use $gongwei-hua 帮我写三句夸领导今天分享的发言。领导性格比较务实，不喜欢太夸张，语气自然一点。
```

```text
Use $tuiju-hua 帮我婉拒朋友借钱。我们关系不错，但他经常拖着不还，我不想伤感情。
```

```text
Use $cuijindu-bushangren 帮我催合作方今天确认方案。对方比较忙，性格直接，语气客气但要推进。
```

```text
Use $wechat-biaoqingbao 看看这句话适合在哪插微信表情包，插什么类型：辛苦你啦，这版已经很清楚了。
```

## 输出风格

默认给：

- 上下文判断
- 对方性格分析
- 稳妥版
- 自然版
- 更正式版或高级一点版
- 不建议这么说
- 分寸提醒

## 全局真实感原则

所有 Skill 都要先判断这句话应该像哪种真实场景：

- 微信私聊：短、松、可有口头语，不必句句完整
- 工作沟通：清楚、克制、有行动点
- 长辈/老师：尊重、具体、少玩梗
- 熟朋友：自然接话，不要为了聪明而硬造梗
- 尴尬场景：先降温，不要继续解释大道理
- 被吐槽像 AI：承认表达太端着，短句收回来

输出时优先像真人会发的话。能一句解决，就不要拆成三段。用户要求“不要句号”“不能损自己”“别夸了”时，严格遵守。

## 设计原则

- 先分析人，再组织话。
- 先看关系，再看场景。
- 先明确目的，再控制分寸。
- 话术要具体、真诚、可发送。
- 对方务实，就少铺垫多说事。
- 对方敏感，就多给台阶少压迫。
- 对方强势，就边界清晰但措辞体面。
- 对方内向，就降低社交压力。
- 对方爱面子，就保留尊重和余地。
- 日常聊天里，短一点、像真人、不解释、不抢戏。

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
  wechat-biaoqingbao/
adapters/
examples/
UNIVERSAL_PROMPTS.md
```

## License

MIT
