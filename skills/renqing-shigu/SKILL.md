---
name: renqing-shigu
description: "Handle Chinese interpersonal communication, social tact, polite wording, relationship-sensitive messages, favors, thanks, apologies, greetings, compliments, workplace phrasing, dinner-table speech, gift messages, WeChat replies, and face-saving language. Use when the user asks for 人情世故, 场面话, 客套话, 情商表达, 怎么说更合适, how to say something tactfully in Chinese, or wants a message based on relationship, context, personality, sincerity, boundaries, and social risk."
---

# 人情世故

Use this skill for relationship-sensitive Chinese communication. It analyzes the context, relationship, the other person's personality, and the user's goal before drafting copy-paste-ready wording.

## First Step: Analyze Context And Personality

Before writing, infer or ask for:

1. **对象身份**: leader, teacher, elder, client, colleague, classmate, friend, partner, stranger.
2. **关系远近**: close, ordinary, formal, superior-subordinate, first contact, long-term relationship.
3. **对方性格**: practical, sensitive, dominant, introverted, face-conscious, humorous, impatient, slow-warming, boundary-conscious.
4. **聊天上下文**: what happened before, current emotion, public/private channel, urgency, pressure.
5. **用户目的**: thank, praise, apologize, refuse, ask for help, follow up, smooth things over, keep boundaries.
6. **风险点**: greasy, vague, too hard, too weak, too flattering, too intimate, too pushy, blame-shifting.

Read `references/context-personality-analysis.md` for high-stakes or unclear situations.
Read `references/high-eq-response-patterns.md` when the user needs to respond to teasing, awkwardness, criticism, misunderstanding, "you sound like AI", "you made me confused", or other live-chat friction.

## Core Principles

1. **先分析人**: match wording to the other person's personality and communication style.
2. **再判断关系**: choose distance, respect level, and warmth.
3. **再判断场景**: thanks, apology, compliment, request, refusal, follow-up, dinner speech, gift message, workplace reply.
4. **再控制分寸**: casual, warm, formal, respectful, humble, concise, enthusiastic.
5. **最后给可发送文本**: write usable wording first, then short cautions.

## Available Subskills

- Compliments and praise: `$gongwei-hua`
- Thanks: `$ganxie-hua`
- Apologies: `$daoqian-hua`
- Refusals: `$tuiju-hua`
- Asking for help: `$qiuren-banshi`
- Dinner-table wording: `$fanju-changmianhua`
- Gift wording: `$songli-huashu`
- Follow-ups: `$cuijindu-bushangren`
- Social comments: `$pengyou-quanquan`
- WeChat sticker placement: `$wechat-biaoqingbao`

## Default Output

Unless the user asks otherwise, provide:

- `上下文判断`: relationship, scene, and risk.
- `对方性格分析`: likely preference and wording strategy.
- `稳妥版`: one broadly safe message.
- `自然版`: a less formal option.
- `更正式版`: a respectful option.
- `不建议这么说`: risky wording to avoid.
- `分寸提醒`: 1-3 short cautions.

## Personality-Based Adjustments

- Practical person: be concise, concrete, and action-oriented.
- Sensitive person: give more context and fewer pressure words.
- Dominant person: respect their position while keeping boundaries clear.
- Introverted person: reduce social pressure and avoid forcing instant replies.
- Face-conscious person: preserve dignity and avoid public correction.
- Humorous person: allow lightness, but keep the main point clear.

## High-EQ Reply Pattern

For awkward or teasing moments, prefer:

```text
接住情绪 + 自嘲/认领一点 + 澄清本意 + 轻松收尾
```

Do not over-explain. When the other person is laughing, confused, or teasing, lower the intensity first.

## Safety And Boundaries

- Do not encourage deception, manipulation, bribery, coercion, harassment, or romantic pressure.
- Do not make compliments sexual, invasive, or body-focused unless the user clearly asks for a harmless intimate context.
- For workplace, teacher-student, elder-junior, or client settings, prefer respectful and specific wording.
- Avoid exaggerated claims that sound fake.
