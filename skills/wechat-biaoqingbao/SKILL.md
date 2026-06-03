---
name: wechat-biaoqingbao
description: "Give Chinese WeChat sticker and emoji placement guidance. Use when the user asks where to insert a WeChat sticker, what kind of sticker to use, how to make a message softer, cuter, less awkward, less formal, or more natural with 表情包, emoji, 微信表情, 小表情, or wants sticker suggestions for compliments, thanks, apologies, refusals, requests, follow-ups, group chats, and Moments comments."
---

# 微信表情包使用指导

Use this skill to suggest where to place a sticker or emoji in a Chinese WeChat message, and what type of sticker fits the relationship and scene.

The goal is not to make every message cute. A good sticker should soften tone, add warmth, reduce awkwardness, or signal friendliness without weakening the main message.

## Before Suggesting

Identify:

- **对象**: leader, teacher, elder, client, colleague, classmate, friend, partner, group chat.
- **关系**: formal, ordinary, familiar, close, ambiguous, first contact.
- **场景**: compliment, thanks, apology, refusal, asking for help, follow-up, dinner, gift, group reply, Moments comment.
- **语气目标**: soften, warm up, ease embarrassment, show sincerity, make it lively, avoid pressure.

## Placement Rules

Read `references/emoji-placement-guide.md` when placement matters.

Default placement:

- Formal or serious message: no sticker, or one gentle sticker at the end.
- Warm casual message: one sticker after the main sentence.
- Light joke: one sticker after the punchline.
- Apology or refusal: use a restrained sticker only after responsibility or boundary is clear.
- Follow-up or reminder: use a softening sticker at the end, not before the request.

## Sticker Type Categories

Use category descriptions rather than exact copyrighted sticker names:

- `微笑/点头`: safe, polite, low intensity.
- `感谢/鞠躬`: gratitude, respect.
- `害羞/挠头`: soften awkwardness.
- `抱拳/拜托`: asking for help, thanks, light respect.
- `加油/鼓掌`: encouragement, praise.
- `可爱小动物/圆脸表情`: friends and casual chats.
- `捂脸/笑哭`: light self-deprecation, not for serious mistakes.
- `收到/OK`: confirmation.

## Output Format

Unless the user asks otherwise, provide:

1. `原句优化`: rewrite the sentence if needed.
2. `插入位置`: show the message with `[表情包: 类型]`.
3. `推荐类型`: 2-3 sticker categories.
4. `不建议`: what not to use and why.

## Boundaries

- Do not suggest flirtatious stickers in workplace, teacher-student, elder-junior, or client settings.
- Do not use funny stickers to cover serious responsibility.
- Do not put stickers before a clear refusal, apology, or request.
- Avoid too many stickers. One is usually enough; two only for close friends.
- For leaders, teachers, elders, and clients, prefer no sticker or a very restrained one.

